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

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Common questions and solutions for scaling Service Fabric clusters](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster#scaling)<br>
* [Why is my VMSS cluster deallocated?](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Issues%20caused%20by%20Deallocating%20a%20VMSS.md)<br>
* [Auto scaling in Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-autoscaling)<br>
* [Cluster scaling options](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-scale-up-down)<br>
* [Scaling clusters programmatically](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-programmatic-scaling)<br>
* [Scaling up primary node types](https://docs.microsoft.com/azure/service-fabric/virtual-machine-scale-set-scale-node-type-scale-out)<br>
* [Scalability of applications](https://docs.microsoft.com/azure/service-fabric/service-fabric-concepts-scalability)<br>
* [Tutorial: Scale a Service Fabric cluster in Azure](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-scale-cluster)<br>
