<properties
	pageTitle="application/upgradeservicenotreachable"
	description="application/upgradeservicenotreachable"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="chiragpa"
    ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608949"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="49cd9fe9-c3d2-4742-9813-6ec983a9002e"
/>

# application/upgradeservicenotreachable

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Service Fabric Endpoint resource](https://docs.microsoft.com/azure/service-fabric/service-fabric-service-manifest-resources#endpoints)<br>
* [Tutorial: Add an HTTPS endpoint to an ASP.NET Core Web API front-end service](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-dotnet-app-enable-https-endpoint)<br>
* [Connecting to other Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-connect-and-communicate-with-services#connecting-to-other-services)<br>
* [Connecting from external Clients](https://docs.microsoft.com/azure/service-fabric/service-fabric-connect-and-communicate-with-services#connections-from-external-clients)<br>
* [Configure Reverse Proxy](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy-configure-secure-communication)<br>
* [Common Networking Scenario for Service Fabric](https://blogs.msdn.microsoft.com/kwill/2016/10/05/azure-service-fabric-common-networking-scenarios/)<br>
