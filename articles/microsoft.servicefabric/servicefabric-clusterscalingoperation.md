<properties
	pageTitle="cluster/scaling"
	description="cluster/scaling"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608960"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="fa5e87fb-f80e-437b-b7f4-e4d13b835934"
/>

# Cluster Scaling

## Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Common questions and solutions for scaling Service Fabric clusters](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#scaling)<br>
* [Why is my VMSS cluster deallocated?](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Issues%20caused%20by%20Deallocating%20a%20VMSS.md)<br>
* [Auto scaling in Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-autoscaling)<br>
* [Cluster scaling options](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-scale-up-down)<br>
* [Scaling clusters programmatically](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-programmatic-scaling)<br>
* [Scaling up primary node types](https://docs.microsoft.com/azure/service-fabric/virtual-machine-scale-set-scale-node-type-scale-out)<br>
* [Scalability of applications](https://docs.microsoft.com/azure/service-fabric/service-fabric-concepts-scalability)<br>
* [Tutorial: Scale a Service Fabric cluster in Azure](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-scale-cluster)<br>
