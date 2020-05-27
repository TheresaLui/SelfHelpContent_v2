<properties
	pageTitle="My application cannot be registered"
	description="My application cannot be registered"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-register"
	displayOrder="7"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# My application cannot be registered

Ensure that you have configured all the required dependencies for service discovery in your POM file. Once configured, the built-in Eureka server endpoint will be automatically injected as environment variable with your application. This allows applications to register  with Eureka server and discover other dependent microservices.

Wait at least 2 minutes for a newly registered instance to start receiving traffic. During these 2 minutes:

1. The first heartbeat, for client registration, occurs 30 seconds after startup.
2. The server updates its response cache every 30 seconds.
3. _Eureka_ client refreshes its cache of registry information every 30 seconds.
4. _Ribbon_ also maintains a local cache to avoid calling the client for every request, requiring another 30 seconds to update.

If you are migrating an existing Spring Cloud based solution to Azure, please make sure your ad-hoc _Eureka_ and _Config Server_ instances are removed (or disabled) to avoid conflicting with the managed instances provided by _Azure Spring Cloud_.

Review the _Eureka_ client logs in _Azure Log Analytics_. For more information about Azure Spring Cloud Diagnostics, please read [Tutorial: Enable Diagnostic Services on your Java Spring app](https://docs.microsoft.com/azure/spring-cloud/diagnostic-services).

To get started with _Azure Log Analytics_, please visit https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal. You will need to query the logs by using [Kusto Query Language](https://docs.microsoft.com/azure/kusto/query/).

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [Tutorial: Enable Diagnostic Services on your Java Spring app](https://docs.microsoft.com/azure/spring-cloud/diagnostic-services)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
