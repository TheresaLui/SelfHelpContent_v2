<properties 
    pageTitle="I am seeing System.XXX Errors in Service Fabric Explorer" 
    description="I am seeing System.XXX Errors in Service Fabric Explorer" 
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    ms.author="pkc"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="2e1f3077-969a-4cd3-8094-a3c3713f7251"
	ownershipId="Compute_ServiceFabric"
/>

# I am seeing System.XXX Errors in Service Fabric Explorer

## **Recommended Steps**

* **System.FM Partition is below target replica or instance count**: Commonly caused when your service is crashing on startup, either due to a missing dependency or a crash in RunAsync or OnActivateAsync. This can also be caused temporarily by something like a node reboot or temporary failure.
* **System.PLB ServiceReplicaUnplacedHealth**: Commonly caused when an application is requesting a higher replica count than there are nodes available in the cluster. This could be because of a misconfigured application manifest, or a cluster node is unavailable due to scale down operations or unexpected node failures.
* **System.PLB MovementsDropped**: Commonly caused when the movement that PLB issued are dropped, and could be mitigated by restarting the replica of the partition.
* **System.PLB NodeCapacityViolation**: Commonly caused when the metrics consumption is over the node capacity, and could be mitigated by adding more nodes to the cluster.
* **System.PLB BalancingUnsuccessful**: Commonly caused when the Load Balancer is unable to balance the cluster further, and could be mitigated by making sure there are equal number of active nodes in FD/UD.
* **System.PLB UpgradePrimarySwapViolation**: Commonly caused when the upgrade is stuck, since primary cannot be swapped. To mitigate this, make sure there is enough capacity on the node.
* **System.PLB ConstraintFixUnsuccessful**: Commonly caused when load balancer unable to balance the cluster further, and could be mitigated by making sure equal number of active nodes of each node type in each FD/UD, and there are nodes with enough capacity.
* **System.PLB ServiceCorrelationError**: Commonly caused when Service affinities cannot form a chain, and to mitigate this issue delete and recreate the service with valid affinity.
* **System.RAP ServiceOpenOperationDuration**: Commonly caused by an exception being thrown in the application's RunAsync method.  Attach a debugger, check Application event logs, or check ETW trace logs for more information.

## **Recommended Documents**

* Most of the System errors are described at [Use system health reports to troubleshoot](https://docs.azure.cn/service-fabric/service-fabric-understand-and-troubleshoot-with-system-health-reports/)
