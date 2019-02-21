<properties
	pageTitle="application/errorandexceptions"
	description="application/errorandexceptions"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="chiragpa"
    ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608950"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="29f37635-647b-435c-b7c5-727d480b9414"
/>

# application/errorandexceptions

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Troubleshoot your local development cluster setup](https://docs.microsoft.com/azure/service-fabric/service-fabric-troubleshoot-local-cluster-setup)<br>
* [Application Monitoring](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-overview#application-monitoring)<br>
* [Tutorial: Troubleshoot Application Failure through Application Insight](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-overview#application-monitoring)<br>
* [Add logging to your Service Fabric application](https://docs.microsoft.com/azure/service-fabric/service-fabric-how-to-diagnostics-log)<br>
* [Troubleshooting Application Upgrades](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)<br>
* [Common exceptions and errors when working with the FabricClient APIs](https://docs.microsoft.com/azure/service-fabric/service-fabric-errors-and-exceptions)<br>
