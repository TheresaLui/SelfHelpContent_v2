<properties
	pageTitle="application/errors or exceptions"
	description="application/errors or exceptions"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32449688"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"
	articleId="b3c9b4b1-0778-4b2d-aa90-035b9c7243b9"
	ownershipId="Compute_ServiceFabric"
/>

# application/errors or exceptions

## **Recommended steps**

Common Failures and Troubleshooting Steps for an Application or Service:

1.	Check Service Fabric Explorer for information about the failure. See "I am seeing System.XXX Errors in Service Fabric Explorer" section and determine which node is failing.
2.	Check Application Event logs or ETW trace logs for exceptions being thrown.
3.	Make sure your async methods (OpenAsync, CloseAsync, RunAsync) correctly handle the CancellationToken since this is how Service Fabric triggers a replica to close.
4.	Make sure all application dependencies are included within your application package.
5.	Common failures are exceptions in entry point methods - RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners, OnCloseAsync, OnOpenAsync
6.	Attach a debugger to your service.

Helpful hints for System.XXX Errors in Service Fabric Explorer:

+ System.FM  Partition is below target replica or instance count : Commonly caused when your service is crashing on startup, either due to a missing dependency or a crash in RunAsync or OnActivateAsync.  Can also be caused temporarily by something like a node reboot or temporary failure.
+ System.PLB ServiceReplicaUnplacedHealth:  Commonly caused when an application is requesting a higher replica count than there are nodes available in the cluster.  This could be because of a misconfigured application manifest, or a cluster node is unavailable due to scale down operations or unexpected node failures.
+ System.PLB MovementsDropped  : Commonly caused when the movement that PLB issued are dropped, and could be mitigated by restarting the replica of the partition
+ System.PLB NodeCapacityViolation : Commonly caused when the metrics consumption is over the node capacity, and could be mitigated by adding more nodes to the cluster
+ System.PLB BalancingUnsuccessful : Commonly caused when the Load Balancer is unable to balance the cluster further, and could be mitigated by making sure there are equal number of active nodes in FD/UD.
+ System.PLB UpgradePrimarySwapViolation : Commonly caused when the upgrade is stuck, since primary cannot be swapped. To mitigate this, make sure there is enough capacity on the node
+ System.PLB ConstraintFixUnsuccessful : Commonly caused when load balancer unable to balance the cluster further, and could be mitigated by making sure equal number of active nodes of each node type in each FD/UD, and there are nodes with enough capacity.
+ System.PLB ServiceCorrelationError : Commonly caused when Service affinities cannot form a chain, and to mitigate this issue delete and recreate the service with valid affinity 
+ System.RAP ServiceOpenOperationDuration:  Commonly caused by an exception being thrown in the application's RunAsync method.  Attach a debugger, check Application event logs, or check ETW trace logs for more information.


## **Recommended documents**
1. [Monitor and diagnose services in a local machine development setup](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/) for how to configure ETW traces in your application
2. [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/) for how to use Visual Studio to debug and view ETW traces for a remote Service Fabric app
3. [Troubleshoot common issues](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-troubleshoot-common-scenarios/)<br>
4. [Diagnostics and performance monitoring for Reliable Actors](https://azure.microsoft.com/documentation/articles/service-fabric-reliable-actors-diagnostics/)<br>
5. [Diagnostic functionality for Stateful Reliable Services](https://azure.microsoft.com/documentation/articles/service-fabric-reliable-services-diagnostics/)
