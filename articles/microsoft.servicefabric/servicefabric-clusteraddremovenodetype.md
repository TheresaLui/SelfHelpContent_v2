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
	cloudEnvironments="public"
	articleId="2cc10d49-53d5-4ef9-83a4-85fe332401d4"
/>

# Add or Remove Node Types

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Common questions and solutions for cluster nodes](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* [Add a new NodeType to a deployed Service Fabric cluster](https://stackoverflow.com/questions/44323742/how-to-add-new-node-type-to-deployed-service-fabric-cluster)<br>
* [Fix missing nodes from a cluster](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/How%20to%20Fix%20one%20missing%20seed%20node.md)<br>
* [Deallocated VMSS cluster issues](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Issues%20caused%20by%20Deallocating%20a%20VMSS.md)<br>
* [Add a new node type to an existing cluster](https://docs.microsoft.com/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype?view=azurermps-6.3.0&viewFallbackFrom=azurermps-4.2.0)<br>
* [Remove a node type from a cluster](https://docs.microsoft.com/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype?view=azurermps-6.3.0)<br>
