<properties 
	pageTitle="Service and Application Management (delete/deploy/upgrade) failures" 
	description="Service and Application Management (delete/deploy/upgrade) failures" 
	service="microsoft.ServiceFabric"
	resource="servicefabric"
	authors="pkcsf"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public"	 
/>
    
# Service and Application Management (delete/deploy/upgrade) failures

## **Common Failures and Troubleshooting Steps**
1. Check Service Fabric Explorer for information about the failure [data-blade: "I am seeing System.XXX Errors in Service Fabric Explorer"] and to determine which node is failing.
2. Check Application Event logs or ETW trace logs for exceptions being thrown.
3. Make sure your async methods (OpenAsync, CloseAsync, RunAsync) correctly handle the CancellationToken since this is how Service Fabric triggers a replica to close.
4. Make sure all application dependencies are included within your application package.
5. Common failures are exceptions in entry point methods - RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners, OnCloseAsync, OnOpenAsync
6. Attach a debugger to your service.
For application related issues, the ETW traces emitted by your application, as well as the Service Fabric ETW traces, are valuable.  See [Monitor and diagnose services in a local machine development setup](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/) for how to configure ETW traces in your application, and [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/) for how to use Visual Studio to debug and view ETW traces for a remote Service Fabric app.
    

## **Errors deleting a service**
When a service is deleted, Service Fabric will first open the service on each of the partitions in order to give the service a chance to clean up. If the service fails to open, or subsequently close, then Service Fabric will detect the failure and prevent the service deletion. First, follow the common failures and troubleshooting steps to determine why the service fails to delete so that you can fix any potential issues in your application.  Once you have determined the cause of the failure you can force the deletion of the service by running Remove-ServiceFabricReplica with the -ForceRemove switch:

	Connect-ServiceFabricCluster clusterendpoint:19000
	$nodes = Get-ServiceFabricNode
	foreach($node in $nodes)
	{	
		$replicas = Get-ServiceFabricDeployedReplica -NodeName $node.NodeName -ApplicationName "fabric:/MyAppName"
		foreach ($replica in $replicas)
		{
		 Remove-ServiceFabricReplica -ForceRemove -NodeName $node.NodeName -PartitionId $replica.Partitionid -ReplicaOrInstanceId $replica.ReplicaOrInstanceId
		}
	}  

## **Errors deploying a service**
1. The majority of deployment failures are caused by exceptions when a service is starting. This could be a missing dependency or exception in the constructor, or an exception in one of the Service Fabric startup methods (RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners). See the 'Common Failures and Troubleshooting Steps' section for how to troubleshoot.
2. Verify that your instance/replica count does not exceed the size of your cluster.

## **Errors upgrading a service**
1. The upgrade process and common issues are documented at [Service Fabric application upgrade](https://azure.microsoft.com/documentation/articles/service-fabric-application-upgrade/)
2. A detailed upgrade troubleshooting workflow can be found at [Troubleshoot application upgrades](https://azure.microsoft.com/documentation/articles/service-fabric-application-upgrade-troubleshooting/)
3. The cluster must be in a healthy state for application upgrades to proceed.  Check Service Fabric Explorer and if there are any warnings investigate and fix those first.
4. In order for an upgrade to be applied,the version numbers must change in the service manifest file.

