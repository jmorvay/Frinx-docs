[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[VPP Operations Manual main page](https://frinxio.github.io/Frinx-docs/FRINX_VPP_Distribution/operations_manual.html)
<!-- TOC -->

- [VPP Distribution: Configuring a Span Port on VPP](#vpp-distribution-configuring-a-span-port-on-vpp)
    - [Install epel-release](#install-epel-release)
    - [Install virtualization packages](#install-virtualization-packages)
    - [Update QEMU to 2.9.0](#update-qemu-to-290)
    - [Update packages and install other tools](#update-packages-and-install-other-tools)
    - [Install VPP](#install-vpp)
    - [Set selinux to permissive](#set-selinux-to-permissive)
    - [Reboot the host to apply changes and boot with updated kernel](#reboot-the-host-to-apply-changes-and-boot-with-updated-kernel)
    - [Run VPP script](#run-vpp-script)
    - [Prepare client VM](#prepare-client-vm)
    - [Prepare server VM](#prepare-server-vm)
    - [Run some traffic](#run-some-traffic)
    - [VPP CLIs for SPAN feature](#vpp-clis-for-span-feature)

<!-- /TOC -->
# VPP Distribution: Configuring a Span Port on VPP
This guide assumes a freshly installed system with CentOS-7-x86_64-Minimal-1708.iso. 
You can access it [here](http://isoredirect.centos.org/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1708.iso) - choose your own mirror.

## Install epel-release
```
yum install epel-release -y
```
## Install virtualization packages
```
yum group install "Virtualization Host" –y
yum install virt-manager libvirt libvirt-python python-virtinst libvirt-client –y
```
## Update QEMU to 2.9.0
1. Install: 
```
yum -y install http://mirror.centos.org/centos/7/virt/x86_64/kVM-common/qemu-img-ev-2.9.0-16.el7_4.13.1.x86_64.rpm http://mirror.centos.org/centos/7/virt/x86_64/kVM-common/qemu-kVM-common-ev-2.9.0-16.el7_4.13.1.x86_64.rpm http://mirror.centos.org/centos/7/virt/x86_64/kVM-common/qemu-kVM-ev-2.9.0-16.el7_4.13.1.x86_64.rpm http://mirror.centos.org/centos/7/virt/x86_64/kVM-common/qemu-kVM-tools-ev-2.9.0-16.el7_4.13.1.x86_64.rpm
```
2. Configure: We need to configure qemu to run as root in `/etc/libvirt/qemu.conf`: 
    - Find the lines *#user = "root"* and *#group = "root"* and uncomment them.

## Update packages and install other tools
```
yum –y update
yum -y install vim #optional
```
## Install VPP
1. First we need to set up the fdio repository: 
```
cat >> /etc/yum.repos.d/fdio-stable1801.repo << EOF [fdio-1801] name=fd.io stable 1801 branch latest merge baseurl=https://nexus.fd.io/content/repositories/fd.io.stable.1801.centos7/ enabled=1 gpgcheck=0 EOF
```
2. 
```
yum -y install vpp vpp-lib vpp-plugins vpp-api-python
```
3. 
```
service vpp start
```
4. Optional: you can setup vpp to start on boot: 
```
chkconfig vpp on
```
5. Verify that HugePages are set up: 
```
grep HugePages /proc/meminfo
```
- HugePages_Total should be 1024, if it isn’t, reboot and start VPP after reboot

## Set selinux to permissive
1. Enter the following:
```
setenforce 0
```
2. Make the config persistent in `/etc/selinux/config`

## Reboot the host to apply changes and boot with updated kernel
```
reboot
```
## Run VPP script
1. VPP must be running
2. Enter the following:
```
chmod 755 tap_monitoring.sh
```
3. 
```
./tap_monitoring.sh
```
The script will create vhost-user interfaces for VMs and also create two Linux namespaces with veth ports with one end in Linux and the other in VPP. All of these are in a bridge domain in VPP. The port mirroring is set up from centos_client’s vhost to ns0’s veth interface.

## Prepare client VM
1. Create disk for the VM: (Substitute 5G for a disk with the size of your choosing)
```
qemu-img create -f qcow2 /var/lib/libvirt/images/centos-client.img 5G
```
2. Download the Centos image mentioned above to `/var/lib/libvirt/images/`: (you can change the following URL to a mirror that’s closer to you)
```
wget -P /var/lib/libvirt/images/ http://ftp.upjs.sk/pub/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-1708.iso
```
3. Create Vhost user socket in VPP:
```
vppctl create vhost socket /tmp/centos_client.sock server
```
4. The VM accepts VNC connections on port 5900, but we need to configure the firewall to allow connection to VNC ports: 
```
firewall-cmd --permanent --zone=public --add-port=5900-5901/tcp firewall-cmd –reload
```
5. Make sure you have a VNC client installed before starting the VM
6. Start the VM (Click [here](centos_client.xml) to access the centos_client.xml file)
```
virsh define centos_client.xml
virsh start centos_client
```
7. Connect to the VNC server running on the host:
    &lt;host-ip&gt;:5900
8. Install the operating system
 - Make sure you configure the network to use the non-vhost interface (its mac should start with  52:54:00).
- Also ensure you configure a root password.
9. After the VM reboots, log in with user root and the password you set up
10. Bring the non-vhost interface 
```
up ifup ens6
```
11. Connect to the on ens6 from the host
12. Modify the `/etc/sysconfig/network-scripts/ifcfg-ens6` script by changing ONBOOT to yes
13. Configure the vhost port:
```
cat > /etc/sysconfig/network-scripts/ifcfg-eth0 << EOF TYPE=Ethernet PROXY_METHOD=none BROWSER_ONLY=no BOOTPROTO=static DEFROUTE=yes IPV4_FAILURE_FATAL=no NM_CONTROLLED=no NAME=eth0 UUID=b8f1a263-9495-43db-9ef1-0393225e4faf DEVICE=eth0 ONBOOT=yes IPADDR=10.0.0.21 NETMASK=255.255.255.0 GATEWAY=10.0.0.1 EOF
```
14. Make sure that the interface names correspond with the script filenames
15. Enable the vhost-user interface 
```
ifup eth0
```
16. Install Iperf3 
```
yum -y install iperf3
```
17. Disable firewall 
```
service firewalld stop 
chkconfig firewalld off
```
## Prepare server VM
We don’t have to go through the whole installation process, because we can just copy the disk and change the IP of the vhost-user port:
1. Enter the following:
```
cp /var/lib/libvirt/images/centos-client.img /var/lib/libvirt/images/centos-server.img
```
2. (Click [here](centos_server.xml) to access the centos_server.xml file)
```
virsh define centos_server.xml 
virsh start centos_server
```
3. The VM will have a different IP on the management port, look in the arp tables for it: 
```
arp –a ? (192.168.122.118) at 52:54:00:c2:13:f9 [ether] on virbr0
```
4. Change the IP in `/etc/sysconfig/network-scripts/ifcfg-eth0` to 10.0.0.22
5. Apply the changes: 
```
ifdown eth0 && ifup eth0
```
## Run some traffic
When both VMs are running we just need to set up Iperf:
1. On the server VM: 
```
iperf –s
```
2. On the client VM: 
```
iperf –c 10.0.0.22
```
3. This will sent packets from client VM to server VM through VPP. VPP will mirror packet from client’s vhost-user interface (vpp0 in linux)
4. Various statistics can be gathered from `/sys/class/net/vpp0/statistics/`, or you can use the script collect_stats.pl (the script from Internet): 
```
chmod 755 collect_stats.pl ./collect_stats.pl
```
## VPP CLIs for SPAN feature
You can investigate the [tap_monitoring.sh](tap_monitoring.sh) script to see which VPP clis were used. There are a few in particular which are unique to this usecase:
```
vppctl set int span <source interface name> l2 destination <destination interface name>
vppctl show int #shows interface names and counters
vppctl show int span #shows the interfaces on which the SPAN feature is configured
```
The SPAN feature is certainly usable on interfaces in l2 mode (the scripts sets all interfaces to be in a bridge domain).