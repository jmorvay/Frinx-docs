[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Operations Manual main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Beryllium/operations_manual.html)
# FRINX ODL Distribution: Features

The FRINX distribution offers the following features:

     odlparent
     yangtools
     mdsal
     controller (without xsql)
     netconf
     aaa
     dlux
     topoprocessing
     snmp
     openflowjava
     openflowplugin
     neutron
     sfc
     ovsdb (without netvirt)
     gbp
     l2switch
     bgpcep
     lispflowmapping
     cli
     daexim
     faas    
     genius
     netvirt
     honeycomb-vbd
     l2vpn
     l3vpn

## To install features
To view a list of available features: Within the karaf console type

 feature:list

To search for a particular feature e.g. restconf you can use grep e.g.

 feature: list |grep restconf

To install a feature:

 feature:install odl-restconf
 feature:install odl-netconf-connector-all

Multiple features can be installed on a single line

 feature:install odl-restconf odl-netconf-connector-all

**Compatibility with other OpenDaylight projects**  
The Frinx ODL Distribution release schedule is tightly synched with OpenDaylight release schedule. The small code delta means that all Beryllium Opendaylight features can be used with the Frinx ODL Distribution. The full list of features can be found here:

<https://www.opendaylight.org/opendaylight-features-list>

**Compatibility between features**  
The link below describes the compatibility between OpenDaylight features.

[https://wiki.opendaylight.org/view/AAA:Beryllium_System_Test_Plan][1]

 [1]: http://wiki.opendaylight.org/view/AAA:Beryllium_System_Test_Plan
