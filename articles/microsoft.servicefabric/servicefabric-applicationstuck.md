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

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Service Fabric Application deployment stuck at "Waiting for upgrade"](https://github.com/Azure/service-fabric-issues/issues/188)<br>
* [Service Fabric Application Stuck in Deleting State](https://github.com/Azure/service-fabric-issues/issues/387)<br>
* [How to remove a Service Fabric application](https://docs.microsoft.com/powershell/module/servicefabric/remove-servicefabricapplication?view=azureservicefabricps)<br>
* [Monitor and diagnose services in a local machine development setup](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/)<br>
* [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/)<br>
* [How to package a Service Fabric application](https://docs.microsoft.com/azure/service-fabric/service-fabric-package-apps)<br>
