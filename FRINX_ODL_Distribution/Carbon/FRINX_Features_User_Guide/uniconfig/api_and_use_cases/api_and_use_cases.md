This document describes API and use cases how UniConfig framework can be used by
external or OpenDaylight application.  
[RESTCONF](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Carbon/FRINX_Features_User_Guide/restconf.html)
is used for API description and REST call examples in this document.

REST calls used in examples can be downloaded as [uniconfig example postman collection](https://github.com/FRINXio/Postman/blob/carbon/development/Uniconfig%20Framework/uniconfig%20example.postman_collection.json).

[More about OpenDaylight controller and its concepts](http://docs.opendaylight.org/en/stable-carbon/developer-guide/controller.html?highlight=restconf)

# UniConfig framework

[Overview and architecture](../architecture/architecture.md)

## Mounting CLI or NETCONF network element
Mounting CLI or NETCONF network element.

![Mount CLI or NETCONF device](drawing/UNM/CLI_NETCONF_mount.png)

### CLI
More information about CLI mounting can be found [here](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/FRINX_Features_User_Guide/cli/cli-service-module.html#mounting-a-cli-device)

[cli-topology.yang](yang/cli-topology.yang)

[Tree representation of cli-topology.yang](yang/cli-topology.html)

### NETCONF
More information about NETCONF mounting can be found [here](http://docs.opendaylight.org/en/stable-carbon/user-guide/netconf-user-guide.html#southbound-netconf-connector)

[netconf-node-topology.yang](yang/netconf-node-topology.yang)

[Tree representation of netconf-node-topology.yang](yang/netconf-node-topology.html)

### Example
Mounting of CISCO IOS-XR device as CLI node.

RPC request:
```
curl -X PUT \
  http://192.168.56.11:8181/restconf/config/network-topology:network-topology/topology/cli/node/IOSXR \
  -H 'content-type: application/json' \
  -d '{
    "network-topology:node" :
    {
      "network-topology:node-id" : "IOSXR",
      "cli-topology:host" : "192.168.1.211",
      "cli-topology:port" : "22",
      "cli-topology:transport-type" : "ssh",
      "cli-topology:device-type" : "ios xr",
      "cli-topology:device-version" : "*",
      "cli-topology:username" : "cisco",
      "cli-topology:password" : "cisco",
      "secret" : "cisco",
      "safe-command-execution": false,
      "cli-topology:keepalive-delay": 30,
      "cli-topology:keepalive-timeout": 30,
      "cli-topology:journal-size": 150,
      "cli-topology:dry-run-journal-size": 150
    }
  }'
```

[more examples in postman collection](https://github.com/FRINXio/Postman/blob/carbon/development/Uniconfig%20Framework/postman.json)

## UniConfig API description

[uniconfig-manager.yang](yang/uniconfig-manager.yang)

*NOTE: mouse hover on elements in tree representation shows description*

[Tree representation of uniconfig-manager.yang](yang/uniconfig-manager.html)

### Config initialization
Initial reading of network element configuration is triggered when unified
mountpoint is discovered. Reading of data from network element is delegated
to unified mountpoint. Only config data are read from unified mountpoint.
If uniconfig node does not exist in config datastore, that means network
element is discovered for a first time, data is stored under uniconfig node
in config and operational datastore. If uniconfig node already exist
in config datastore, data is stored only to operational datastore.

![Initial reading](drawing/UNM/initial_read.png)

### RPC sync-from-network
Purpose of this RPC is to synchronize configuration from network
elements to uniconfig nodes in operational datastore.

![RPC sync-from-network](drawing/UNM/RPC_sync-from-network.png)

#### Example
RPC input contains list of uniconfig nodes where configuration should be
refreshed.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:sync-from-network \
  -H 'content-type: application/json' \
  -d '{
    "input": {
        "node-to-sync": [
            {
                "node-id": "IOSXR"
            }
        ]
    }
}'
```

RPC response - success:

```
{
    "output": {
        "node-sync-status-results": {
            "node-sync-status-result": [
                {
                    "nodeId": "IOSXR"
                }
            ]
        }
    }
}
```

### RPC commit
External or ODL application stores intended configuration under nodes
in uniconfig topology. Trigger for execution of configuration is RPC
commit.

[List of supported configuration data](https://github.com/FRINXio/translation-units-docs/tree/master/Configuration%20datasets)

Successful RPC commit is on figure below.

![RPC commit success case](drawing/UNM/RPC_commit_success.png)

Failed RPC commit with automatic rollback is on figure below.

![RPC commit fail case](drawing/UNM/RPC_commit_fail.png)

#### Example
RPC commit has no input and output describes result of commit.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:commit
```

RPC response - success:

```
{
    "output": {
        "overall-configuration-status": "complete",
        "node-config-results": {
            "node-config-result": [
                {
                    "nodeId": "IOSXR",
                    "configuration-status": "complete"
                }
            ]
        }
    }
}
```

### RPC create-snapshot
RPC creates snapshot of uniconfig topology. This snapshot can be used 
for manual rollback.

![RPC create-snapshot](drawing/UNM/RPC_create-snapshot.png)

#### Example
RPC input contains name for topology snapshot. RPC output contains
result of operation.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:create-snapshot \
  -H 'content-type: application/json' \
  -d '{
    "input": {
        "name": "snapshot1"
    }
}'
```

RPC response - success:

```
{
    "output": {
        "result": "complete"
    }
}
```

### RPC delete-snapshot
RPC removes snapshot from CONF DS.

![RPC delete-snapshot](drawing/UNM/RPC_delete-snapshot.png)

#### Example
RPC input contains name of topology snapshot which should be removed.
PRC output contains result of operation.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:delete-snapshot \
  -H 'content-type: application/json' \
  -d '{
    "input": {
        "name": "snapshot1"
    }
}'
```

RPC response - success:

```
{
    "output": {
        "result": "complete"
    }
}
```

### RPC calculate-diff
This RPC creates diff between actual uniconfig topology and intended
uniconfig topology.

![RPC calculate-diff](drawing/UNM/RPC_calculate-diff.png)

#### Example
RPC input is empty and output contains list of statements representing
diff.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:calculate-diff \
  -H 'accept: application/xml' \
```

RPC response - success:

```
<output xmlns="urn:opendaylight:params:xml:ns:yang:uniconfig:manager">
    <node-with-diff>
        <node-id>IOSXR</node-id>
        <created-data>
            <path xmlns:c="http://frinx.openconfig.net/yang/interfaces" xmlns:b="http://frinx.openconfig.net/yang/uniconfig-topology" xmlns:d="http://frinx.openconfig.net/yang/interfaces/ethernet" xmlns:a="urn:TBD:params:xml:ns:yang:network-topology">/a:network-topology/a:topology[a:topology-id='uniconfig']/a:node[a:node-id='IOSXR']/b:configuration/c:interfaces/c:interface[c:name='GigabitEthernet0/0/0/3']/d:ethernet/d:config</path>
            <data>{
  "frinx-openconfig-if-ethernet:config": {
    "frinx-lacp-lag-member:lacp-mode": "ACTIVE",
    "frinx-lacp-lag-member:interval": "SLOW",
    "frinx-openconfig-if-aggregate:aggregate-id": "Bundle-Ether10",
    "auto-negotiate": true,
    "enable-flow-control": false
  }
}</data>
        </created-data>
    </node-with-diff>
</output>
```

### RPC replace-config-with-operational
RPC replaces uniconfig topology in config datastore with uniconfig
topology from operational datastore.  

![RPC replace-config-with-operational](../api_and_use_cases/drawing/UNM/RPC_replace-config-with-operational.png)

#### Example
There is no RPC input and PRC output contains result of operation.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:replace-config-with-operational
```

RPC response - success:

```
{
    "output": {
        "result": "complete"
    }
}
```

### RPC replace-config-with-snapshot
RPC replaces uniconfig topology in config datastore with snapshot from
operational datastore.  

![RPC replace-config-with-snapshot](../api_and_use_cases/drawing/UNM/RPC_replace-config-with-snapshot.png)

#### Example
RPC input contains name of topology snapshot which should replace uniconfig
topology in config datastore. PRC output contains result of operation.

RPC request:
```
curl -X POST \
  http://192.168.56.11:8181/restconf/operations/uniconfig-manager:replace-config-with-snapshot \
  -H 'content-type: application/json' \
  -d '{
    "input": {
        "name": "snapshot1"
    }
}'
```

RPC response - success:

```
{
    "output": {
        "result": "complete"
    }
}
```
