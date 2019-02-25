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

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Service Fabric Application Upgrade Concepts and Settings](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade)<br>
* [Parameter applied during Application upgrade](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters)<br>
* [Application upgrade scenarios](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-advanced)<br>
* [Service Fabric Application Lifecycle](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-lifecycle)<br>
* [Troubleshoot Application upgrades](https://azure.microsoft.com/documentation/articles/service-fabric-application-upgrade-troubleshooting/)<br>
* [Rolling back Application upgrades](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-advanced#rolling-back-application-upgrades)<br>
