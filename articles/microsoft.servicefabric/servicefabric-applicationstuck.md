<properties
	pageTitle="application/stuck"
	description="application/stuck"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="chiragpa"
    ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608961"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="24a81ccd-f5d0-4f6a-ab14-c0e5a0e92ebd"
/>

# application/stuck

## **Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters**
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Service Fabric Application deployment stuck at "Waiting for upgrade"](https://github.com/Azure/service-fabric-issues/issues/188)<br>
* [Service Fabric Application Stuck in Deleting State](https://github.com/Azure/service-fabric-issues/issues/387)<br>
* [How to remove a Service Fabric application](https://docs.microsoft.com/powershell/module/servicefabric/remove-servicefabricapplication?view=azureservicefabricps)<br>
* [Monitor and diagnose services in a local machine development setup](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/)<br>
* [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/)<br>
* [How to package a Service Fabric application](https://docs.microsoft.com/azure/service-fabric/service-fabric-package-apps)<br>
