[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Carbon Release Notes main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Carbon/release_notes.html)

This document describes the latest changes, additions, known issues, and fixes for the Frinx ODL Distribution.<!--more-->

**Update - currently the "./bin/status" command does not operate correctly - please refrain from using until further notice. We are working on a resolution to this issue.**

**Note that FRINX ODL distribution 3.1.1 requires Java 8**  
To install Java:  
Ubuntu: In a terminal type

    sudo apt-get install openjdk-8-jre

CentOS: In a terminal type

    sudo yum install java-1.8.0-openjdk

#### Known Issues

1. L2 VPN and L3 VPN service applications stay unchanged and are working as in Milestone 1 & 2 (XR supported).
2. “Line card” information is not implemented for IOS devices.
3. In older IOS versions, parsing in show IP route static not fully supported on IOS 12.X.
4. Configuration commands for L3VPN/with BGP for IOS XR are missing.
5. Configuration commands for L3VPN/with OSPF for IOS XR are missing.
6. Show commands for OSPF routing are not working with the version IOS XE 16.7.1.
7. Rollback is not working when L2VPN update fails.
8. VRF crud tests are missing, will be created in January 2018.
9. L3VPN OSPF, L3VPN BGP, VPWS and VPLS will be tested in January 2018.

#### Opendaylight Carbon Release Notes

The Frinx controller 3.1.1 is based on OpenDaylight Carbon.

<https://wiki.opendaylight.org/view/Simultaneous_Release/Carbon/Release_Notes>
<https://wiki.opendaylight.org/view/Simultaneous_Release:Carbon_Release_Plan>
<https://wiki.opendaylight.org/view/BGP_LS_PCEP:Carbon_Release_Notes>
