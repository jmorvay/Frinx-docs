# Connecting to an OpenFlow Switch

<!-- TOC START min:1 max:3 link:true update:true -->
- [Connecting to an OpenFlow Switch](#connecting-to-an-openflow-switch)
  - [Option A: Installing Openflow features using the karaf console##](#option-a-installing-openflow-features-using-the-karaf-console)
  - [Option B: Installing Openflow features using the Frinx UI##](#option-b-installing-openflow-features-using-the-frinx-ui)
  - [Set up Mininet##](#set-up-mininet)

<!-- TOC END -->

In OpenDaylight, OpenFlow is implemented by the following features: odl-l2switch (and dependencies), openflowplugin and openflowjava. These can be installed in one of the following two ways:

##Option A: Installing Openflow features using the karaf console##  
Open or connect to a karaf console and type:

    feature:install odl-l2switch-all  
    feature:install odl-restconf  
    feature:install odl-mdsal-apidocs  
    feature:install odl-dlux-all  


(odl-dlux-all is installed by default)

##Option B: Installing Openflow features using the Frinx UI##  
Open the Web UI and navigate to: [http://localhost:8181/index.html#/featuremgr/index ][1]Use the filter functionality to verify which features are installed ![image](1-1030x422.png)
Verify that `odl-l2switch-all`, `odl-restconf`, `odl-mdsal-apidocs`, `odl-dlux-all` are installed. As shown in the screenshot above, an installed feature is indicated by both a tick in the Installed column and a trashcan in the Install/Uninstall column. The Frinx UI should be used when you wish to uninstall a feature, as uninstalling using the Karaf console is not currently supported and could cause undesirable behavior.

##Set up Mininet##  
The easiest way to do this is to download a mininet virtual machine (VM) from <https://github.com/mininet/mininet/wiki/Mininet-VM-Images> Then configure your environment so that you can connect to the Mininet VM from the machine hosting the Frinx controller. For example: if the Frinx ODL Distribution is hosted at 10.10.199.149 and Mininet is installed at 10.10.199.20, a ping should work in both directions.  
Use the following command to start Mininet, replacing < your controller ip > with the IP address of the machine hosting the Frinx controller.

    sudo mn --topo linear,3 --mac --controller=remote,ip=< your controller ip >,port=6633 --switch ovsk,protocols=OpenFlow13  


If the command is successful, then if you go to

<http://10.10.199.149:8181/index.html#/topology> you will see something like the screenshot below: ![image2](2-1030x620.png)
The OpenDaylight userguide describes alternative ways to start mininet: [https://nexus.opendaylight.org/content/sites/site/org.opendaylight.docs/master/userguide/manuals/userguide/bk-user-guide/content/\_create\_a_network_using_mininet.html][2]

 [1]: http://localhost:8181/index.html#/featuremgr/index
 [2]: https://nexus.opendaylight.org/content/sites/site/org.opendaylight.docs/master/userguide/manuals/userguide/bk-user-guide/content/_create_a_network_using_mininet.html
