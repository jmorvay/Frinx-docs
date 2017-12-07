[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Operations Manual main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Boron/operations_manual.html)
<!-- TOC -->

- [Clustering: Overview](#clustering-overview)
    - [High availability (HA)](#high-availability-ha)
    - [Data persistence](#data-persistence)
    - [Scaling](#scaling)
    - [Single node clustering](#single-node-clustering)
    - [Multiple node clustering](#multiple-node-clustering)
        - [a. Setting up](#a-setting-up)
        - [b. Info on data shards](#b-info-on-data-shards)
        - [c. Info on seed nodes](#c-info-on-seed-nodes)
        - [d. Info on clustering functionality](#d-info-on-clustering-functionality)
        - [e. Deploying a cluster automatically](#e-deploying-a-cluster-automatically)

<!-- /TOC -->
# Clustering: Overview
Clustering enables multiple instances of the Frinx ODL Distribution to work together as one entity. Data from the in-memory MD-SAL tree is split into smaller sub-trees (inventory, topology, and default) and distributed across the machines (referred to as nodes) which are part of the cluster.

This offers a number of benefits:

## High availability (HA)
If you have multiple instances running and one crashes, you would still have the other instances working and available.

## Data persistence  
You will not lose any data gathered by your controller after a manual restart or a crash. By restarting Frinx ODL, you can use the persisted data to reinstate shards to their previous state.

## Scaling  
If you have multiple Frinx ODL instances running as a cluster, you can potentially do more work or store more data. 

*The following sections describe how to set up clustering on both individual and multiple Frinx ODL distributions.*

## Single node clustering  
To enable clustering on a single machine running the Frinx ODL distribution:  

1\. Run Karaf: In your main Frinx ODL directory, type  

    ./bin/karaf  

2.\ In the karaf terminal, type:

    feature:install odl-mdsal-clustering

## Multiple node clustering  
### a. Setting up  
To run the Frinx ODL distribution in a three node cluster (that is, on three machines), do the following:  
1\. Determine the three machines (nodes) that will make up the cluster and copy the Frinx ODL distribution to each of those machines.  

2\. Unzip the controller distribution.  
 
3\. Run Karaf: In your main Frinx ODL directory, type

    ./bin/karaf  

4.\ In the karaf terminal, type:

    feature:install odl-mdsal-clustering

5\. On each machine, open the `{Frinx ODL main}/configuration/initial/akka.conf` file.

In the following line, replace *127.0.0.1* with the hostname or IP address of the machine on which the Frinx ODL distribution will run:

    netty.tcp {hostname = "127.0.0.1"}`

In the following line, replace *127.0.0.1* with the hostname or IP address of either of the other two machines (without repeating the same IP address):

    cluster {seed-nodes = ["akka.tcp://opendaylight-cluster-data@127.0.0.1:2550"]}

In the following line, replace member-1 with member-2 or member-3 as appropriate so that you have a different member specified on each of the three machines.  

    roles = ["member-1"]  

6\. On each machine, open the `{Frinx ODL main}/configuration/initial/module-shards.conf` file and update the following line so that the replicas member number corresponds to the roles member number defined above (member-1, member-2 or member-3, depending on the machine).

    replicas = ["member-1"]

You can now use any of the three member nodes (machines) to access the data residing in the datastore. For example, if you want to view information about the shard designated as *member-1* on a node, query the shard’s data by making the following HTTP request: *HTTP Method: GET* *HTTP URL:* <http://localhost:8181/jolokia/read/org.opendaylight.controller:Category=Shards,name=member-1-shard-inventory-config,type=DistributedConfigDatastore>

If prompted, enter admin as both the username and password.  
*HTTP: EXPECTED RESPONSE*  
This request should return the following information:  
{ "timestamp": 1410524741, "status": 200, "request": { "mbean": "org.opendaylight.controller:Category=Shards,name=member-1-shard-inventory-config,type=DistributedConfigDatastore", "type": "read" }, "value": { "ReadWriteTransactionCount": 0, "LastLogIndex": -1, "MaxNotificationMgrListenerQueueSize": 1000, "ReadOnlyTransactionCount": 0, "LastLogTerm": -1, "CommitIndex": -1, "CurrentTerm": 1, "FailedReadTransactionsCount": 0, "Leader": "member-1-shard-inventory-config", "ShardName": "member-1-shard-inventory-config", "DataStoreExecutorStats": { "activeThreadCount": 0, "largestQueueSize": 0, "currentThreadPoolSize": 1, "maxThreadPoolSize": 1, "totalTaskCount": 1, "largestThreadPoolSize": 1, "currentQueueSize": 0, "completedTaskCount": 1, "rejectedTaskCount": 0, "maxQueueSize": 5000 }, "FailedTransactionsCount": 0, "CommittedTransactionsCount": 0, "NotificationMgrExecutorStats": { "activeThreadCount": 0, "largestQueueSize": 0, "currentThreadPoolSize": 0, "maxThreadPoolSize": 20, "totalTaskCount": 0, "largestThreadPoolSize": 0, "currentQueueSize": 0, "completedTaskCount": 0, "rejectedTaskCount": 0, "maxQueueSize": 1000 }, "LastApplied": -1, "AbortTransactionsCount": 0, "WriteOnlyTransactionCount": 0, "LastCommittedTransactionTime": "1969-12-31 16:00:00.000", "RaftState": "Leader", "CurrentNotificationMgrListenerQueueStats": [] } }

The key thing here is the name of the shard. Shard names are structured as follows:

    <member-name>-shard-<shard-name-as-per-configuration>-<store-type>  

Here are a couple of sample data short names: • member-1-shard-topology-config • member-2-shard-default-operational. 

**We recommend a minimum of three nodes** because a two node cluster will become unoperational if one node goes down.

### b. Info on data shards   
*Data shards* house all or a certain segment of a module’s data. For example, one shard can contain all of a module’s inventory data while another shard contains all of its topology data.

If you do not specify a module in the `modules.conf` file and do not specify a shard in `module-shards.conf`, then (by default) all the data is placed onto the default shard (which must also be defined in `module-shards.conf` file). Each shard has replicas configured, which can be specified in the `module-shards.conf` file. 

If you have a three node cluster on which HA is enabled, a replica of every defined data shard must be running on all three cluster nodes. This is because OpenDaylight’s clustering implementation requires a majority of the defined shard replicas to be running in order to function. 

If you only define data shard replicas on two of the cluster nodes and one of those goes down, the corresponding data shards will not function. 

If you have a three node cluster and have defined replicas for a data shard on each of those nodes, that shard will still function even if only two of the cluster nodes are running. *Note that if one of those two nodes go down, your controller will no longer be operational.*

### c. Info on seed nodes  
We recommend that you have multiple seed nodes configured. After a cluster member is started, it sends a message to all of its seed nodes. The cluster member then sends a join command to the first seed node that responds. If none of its seed nodes reply, the cluster member repeats this process until it successfully establishes a connection or it is shutdown.

### d. Info on clustering functionality 
After a node becomes unreachable, it remains down for a configurable period of time (10 seconds by default). Once a node goes down, you need to restart it so that it can rejoin the cluster. Once a restarted node joins a cluster, it will synchronize with the lead node automatically. You can run a two node cluster for functional testing, but for HA testing you need to run all three nodes.

### e. Deploying a cluster automatically  
The cluster can be also deployed automatically using a script developed by the OpenDaylight integration project. The script is available from their Git repository.

    git clone https://git.opendaylight.org/gerrit/integration/test.git

    cd test/tools/clustering/cluster-deployer/

Instructions for use are available at:

<https://wiki.opendaylight.org/view/Running_and_testing_an_OpenDaylight_Cluster>

 [1]: https://nexus.opendaylight.org/content/sites/site/org.opendaylight.docs/master/userguide/manuals/userguide/bk-user-guide/content/_setting_up_clustering_on_an_opendaylight_controller.html
