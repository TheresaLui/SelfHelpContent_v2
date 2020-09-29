<properties
	pageTitle="cluster/clusteraddremovenodetype"
	description="cluster/clusteraddremovenodetype"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608936"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="2cc10d49-53d5-4ef9-83a4-85fe332401d4"
	ownershipId="Compute_ServiceFabric"
/>

# Add or Remove Node Types

## Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters

As of Service Fabric runtime version 6.4.644 for Linux clusters, a previous issue with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Common questions and solutions for cluster nodes](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* [Add a new NodeType to a deployed Service Fabric cluster](https://stackoverflow.com/questions/44323742/how-to-add-new-node-type-to-deployed-service-fabric-cluster)<br>
* [Fix missing nodes from a cluster](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/How%20to%20Fix%20one%20missing%20seed%20node.md)<br>
* [Deallocated VMSS cluster issues](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Issues%20caused%20by%20Deallocating%20a%20VMSS.md)<br>
* [Add a new node type to an existing cluster](https://docs.microsoft.com/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype?view=azurermps-6.3.0&viewFallbackFrom=azurermps-4.2.0)<br>
* [Remove a node type from a cluster](https://docs.microsoft.com/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype?view=azurermps-6.3.0)<br>
