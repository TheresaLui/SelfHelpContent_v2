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

## **Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters**
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

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
