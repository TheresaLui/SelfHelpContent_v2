<properties
	pageTitle="cluster/deploymentordeletion"
	description="cluster/deploymentordeletion"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608945"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="a5eaf9ea-059a-45b1-b685-bc78706cf440"
/>

# Cluster Deployment or Deletion

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Common questions and solutions for cluster nodes](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#nodes)<br>
* [Create Service Fabric clusters in the Azure portal](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-via-portal)<br>
* [Create Service Fabric clusters with ARM](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-via-arm)<br>
* [Create standalone Service Fabric clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-for-windows-server)<br>
* [Delete a Service Fabric cluster and resources on Azure](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-delete)<br>
* [Deploy a Service Fabric Windows cluster into an Azure virtual network](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-create-vnet-and-windows-cluster)<br>
* [Service Fabric cluster templates](https://github.com/Azure-Samples/service-fabric-cluster-templates)<br>
* [Capacity planning consideration for Service Fabric clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-capacity)<br>
* [Connect to a Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-connect-to-secure-cluster)<br>
