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

## **Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters**
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Common questions and solutions for patch orchestration](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/tree/master/Cluster)<br>
* [Patch orchestration application issues](https://github.com/Azure/service-fabric-issues/issues/290)<br>
* [Patch orchestration telemetry](https://github.com/Azure/service-fabric-issues/issues/617)<br>
* [Patch Windows for your Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application)<br>
* [Patch Linux for your Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application-linux)<br>
* [Patch orchestration FAQ](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application#frequently-asked-questions)<br>
