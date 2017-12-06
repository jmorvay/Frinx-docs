[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Operations Manual main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Carbon/operations_manual.html)
<!-- TOC -->

- [Clustering: Overview](#clustering-overview)
    - [Scaling](#scaling)
    - [High availability](#high-availability)
    - [Data persistence](#data-persistence)
    - [Data sharding](#data-sharding)
    - [Single node clustering](#single-node-clustering)
    - [Multiple node clustering](#multiple-node-clustering)
        - [a. Setting up](#a-setting-up)
        - [b. Deploying a cluster automatically](#b-deploying-a-cluster-automatically)

<!-- /TOC -->
# Clustering: Overview
Clustering is a mechanism that enables multiple processes and programs to work together as one entity. For example, a Google Web search is in fact processed by thousands of web servers connected in a cluster. Similarly, you can have multiple instances of the OpenDaylight controller working together as one entity. There are a number of uses for clustering:

## Scaling  
If you have multiple controllers running, you can potentially do more work with or store more data on those controllers if they are clustered. You can also break your data into smaller chunks (known as shards) and either distribute that data across the cluster or perform certain operations on certain members of the cluster.

## High availability  
If you have multiple controllers running and one crashes, you would still have the other instances working and available.

## Data persistence  
You will not lose any data gathered by your controller after a manual restart or a crash. 

## Data sharding  
The in-memory MD-SAL tree is broken up into a number of smaller sub-trees (inventory, topology, and default).

All of the data available on defined data shards is stored on a disk. By restarting Frinx ODL, you can use the persisted data to reinstate those shards to their previous state.

*The following sections describe how to set up clustering on both individual and multiple Frinx ODL distributions.*

## Single node clustering  
To enable clustering on a single machine running the Frinx ODL distribution:  

1\. In the `{Frinx ODL main}/etc` directory, edit the file `org.apache.karaf.features.cfg`: Find the line that begins with '#odlFeaturesBoot'. Remove '#' and add the feature 'odl-mdsal-clustering' (you can keep any other features you currently have listed, just use a comma to separate features). The format should be as follows:

odlFeaturesBoot=odl-mdsal-clustering

Save the file.  
2\. Run Karaf: In your main Frinx ODL directory, type  

    ./bin/karaf  

## Multiple node clustering  
### a. Setting up    
*(See next section for deployment considerations)*.  
To run the Frinx ODL distribution in a three node cluster (that is, on three machines), do the following:  
1\. Determine the three machines (nodes) that will make up the cluster and copy the Frinx ODL distribution to each of those machines.  
2\. Unzip the controller distribution.  
 
3\. In the `{Frinx ODL main}/etc` directory, edit the file `org.apache.karaf.features.cfg`: Find the line that begins with '#odlFeaturesBoot'. Remove '#' and add the feature 'odl-mdsal-clustering' (you can keep any other features you currently have listed, just use a comma to separate features). The format should be as follows:

odlFeaturesBoot=odl-mdsal-clustering

Save the file.

4\. Run Karaf: In your main Frinx ODL directory, type

    ./bin/karaf 

5\. On each machine, open the `{Frinx ODL main}/configuration/initial/akka.conf` file.

In the following line within the file, replace *127.0.0.1* with the hostname or IP address of the machine on which the Frinx ODL distribution will run:

    netty.tcp {hostname = "127.0.0.1"}`

In the following line within the file, replace *127.0.0.1* with the hostname or IP address of any of the machines that will be part of the cluster:

    cluster {seed-nodes = ["akka.tcp://opendaylight-cluster-data@127.0.0.1:2550"]}

In the following line within the file, replace member-1 with member-2 or member-3 so that you have a different member specified on each of the three machines.  

    roles = ["member-1"]  

6\. On each machine, open the `{Frinx ODL main}/configuration/initial/module-shards.conf` file and update the following line so that the replicas member number corresponds to the roles member number defined above.

    replicas = ["member-1"]

The Frinx ODL distribution can now run in a three node cluster. Use any of the three member nodes to access the data in the datastore. For example, if you want to view information about the shard designated as *member-1* on a node, could can do so by querying the shard’s data by making the following HTTP request: *HTTP Method: GET* *HTTP URL:* <http://localhost:8181/jolokia/read/org.opendaylight.controller:Category=Shards,name=member-1-shard-inventory-config,type=DistributedConfigDatastore>

If prompted, enter admin as both the username and password.  
*HTTP: EXPECTED RESPONSE*  
This request should return the following information:  
{ "timestamp": 1410524741, "status": 200, "request": { "mbean": "org.opendaylight.controller:Category=Shards,name=member-1-shard-inventory-config,type=DistributedConfigDatastore", "type": "read" }, "value": { "ReadWriteTransactionCount": 0, "LastLogIndex": -1, "MaxNotificationMgrListenerQueueSize": 1000, "ReadOnlyTransactionCount": 0, "LastLogTerm": -1, "CommitIndex": -1, "CurrentTerm": 1, "FailedReadTransactionsCount": 0, "Leader": "member-1-shard-inventory-config", "ShardName": "member-1-shard-inventory-config", "DataStoreExecutorStats": { "activeThreadCount": 0, "largestQueueSize": 0, "currentThreadPoolSize": 1, "maxThreadPoolSize": 1, "totalTaskCount": 1, "largestThreadPoolSize": 1, "currentQueueSize": 0, "completedTaskCount": 1, "rejectedTaskCount": 0, "maxQueueSize": 5000 }, "FailedTransactionsCount": 0, "CommittedTransactionsCount": 0, "NotificationMgrExecutorStats": { "activeThreadCount": 0, "largestQueueSize": 0, "currentThreadPoolSize": 0, "maxThreadPoolSize": 20, "totalTaskCount": 0, "largestThreadPoolSize": 0, "currentQueueSize": 0, "completedTaskCount": 0, "rejectedTaskCount": 0, "maxQueueSize": 1000 }, "LastApplied": -1, "AbortTransactionsCount": 0, "WriteOnlyTransactionCount": 0, "LastCommittedTransactionTime": "1969-12-31 16:00:00.000", "RaftState": "Leader", "CurrentNotificationMgrListenerQueueStats": [] } }

The key thing here is the name of the shard. Shard names are structured as follows:

    <member-name>-shard-<shard-name-as-per-configuration>-<store-type>  

Here are a couple of sample data short names: • member-1-shard-topology-config • member-2-shard-default-operational.

**We recommend a minimum of three machines** because a two node cluster will become unoperational if one node goes down.

### b. Deploying a cluster automatically  
The cluster can be also deployed automatically using a script developed by the OpenDaylight integration project. The script is available from their Git repository.

    git clone https://git.opendaylight.org/gerrit/integration/test.git

    cd test/tools/clustering/cluster-deployer/

Instructions for use are available at:

<https://wiki.opendaylight.org/view/Running_and_testing_an_OpenDaylight_Cluster>

 [1]: https://nexus.opendaylight.org/content/sites/site/org.opendaylight.docs/master/userguide/manuals/userguide/bk-user-guide/content/_setting_up_clustering_on_an_opendaylight_controller.html
