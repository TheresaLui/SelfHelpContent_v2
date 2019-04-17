<properties
	pageTitle="application/upgrade"
	description="application/upgrade"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="chiragpa"
    ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608939"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="c348fb41-7b43-4084-9f1d-151e8307eb9a"
/>

# application/upgrade

## Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters
As of Service Fabric runtime version 6.4.644 for Linux clusters a previous issue with with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Service Fabric Application Upgrade Concepts and Settings](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade)<br>
* [Parameter applied during Application upgrade](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters)<br>
* [Application upgrade scenarios](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-advanced)<br>
* [Service Fabric Application Lifecycle](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-lifecycle)<br>
* [Troubleshoot Application upgrades](https://azure.microsoft.com/documentation/articles/service-fabric-application-upgrade-troubleshooting/)<br>
* [Rolling back Application upgrades](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-advanced#rolling-back-application-upgrades)<br>
