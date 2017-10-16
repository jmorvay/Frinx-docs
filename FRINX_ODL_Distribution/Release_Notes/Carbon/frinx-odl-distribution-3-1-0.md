[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Carbon Release Notes main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Release_Notes/Carbon.html)
    
This document describes the latest changes, additions, known issues, and fixes for the Frinx ODL Distribution.<!--more-->

**Note that FRINX ODL distribution 3.1.0 requires Java 8**

#### New Features, Improvements

1.  Clustering changes:
    
    * Reduced number of shards to 4: default-config, default-operational, prefix-configuration-shard-config, prefix-configuration-shard-operational
    * Modified raft election mechanism to move shard leaders to the same node, all shards will eventually have leaders on one node
    * Entity ownership is based on which node hosts the shard leaders

2.  Modified daexim, including startup changes, described at https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/FRINX_Features_Developer_Guide/daexim.html
    
3. cli, unified-topology, l2vpn, l3vpn projects added


#### Known Issues

1.  daexim: 
    *   daexim import does not work.
2.  odl-netconf-clustered-topology: 
    *   contains critical bugs and is not intended for production use, so odl-netconf-topology was modified so that it can work in cluster. Due to the fact that each node maintains its own connection to netconf devices, connection status reported in operational datastore might be overwritten and not reflect actual state.
3.  restconf/operational/entity-owners:
    *   entity-owners contains no data as entity ownership service was rewritten. Entity owners are assigned to the same node that hosts shard leaders.
4.  Operational state of IOS device cannot be read when VRF is configured on the device and the device is mounted via SSH.


#### Opendaylight Carbon Release Notes

The Frinx controller 3.1.0 is based on OpenDaylight Carbon.

<https://wiki.opendaylight.org/view/Simultaneous_Release/Carbon/Release_Notes>
<https://wiki.opendaylight.org/view/Simultaneous_Release:Carbon_Release_Plan>
<https://wiki.opendaylight.org/view/BGP_LS_PCEP:Carbon_Release_Notes>
