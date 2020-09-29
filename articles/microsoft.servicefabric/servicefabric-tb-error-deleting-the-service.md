<properties 
	pageTitle="Errors deleting a service" 
	description="Errors deleting a service" 
	service="microsoft.servicefabric"
	resource="clusters"
	authors="pkcsf"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public,BlackForest,Fairfax,MoonCake, usnat, ussec"	 
	articleId="455069fa-7de5-47cd-9d18-786f1e7ee2ba"
	ownershipId="Compute_ServiceFabric"
/>

# Errors deleting a service 

## **Recommended steps**
1.	Follow the steps mentioned under “Common Failures and Troubleshooting Steps for Application/Service” section to determine why the service fails to delete, so that you can fix any potential issue in your application
2.	Once you have determined the cause of the failure you can force the deletion of the service by running Remove-ServiceFabricReplica with the -ForceRemove switch:
          
```powershell
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
```

