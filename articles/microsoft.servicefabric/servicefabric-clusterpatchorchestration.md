<properties
	pageTitle="cluster/patchorchestration"
	description="cluster/patchorchestration"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="ChiragPavecha"
	ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608955"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="893c6d1e-97d8-4d49-af44-313593e11767"
/>

# Cluster Patch Orchestration

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Common questions and solutions for patch orchestration](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster)<br>
* [Patch orchestration application issues](https://github.com/Azure/service-fabric-issues/issues/290)<br>
* [Patch orchestration telemetry](https://github.com/Azure/service-fabric-issues/issues/617)<br>
* [Patch Windows for your Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application)<br>
* [Patch Linux for your Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application-linux)<br>
* [Patch orchestration FAQ](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application#frequently-asked-questions)<br>
