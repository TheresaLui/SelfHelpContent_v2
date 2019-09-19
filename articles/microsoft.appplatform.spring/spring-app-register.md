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
	cloudEnvironments="public"
/>

# My application cannot be registered

In most case, it is because you have not configured the required dependencies for service discovery(`https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/dev-guide.md#service-discovery`) in your pom file. After configured, the built-in Eureka server endpoint will be automatically injected as environment variable with your application. Then applications will be able to register themselves with Eureka server and discover other dependent microservices.

Please wait at least 2 minutes before a newly registered instance start receiving traffic. This is because of a few reasons:

1. The first heartbeat happens 30 seconds after startup, this heartbeat is for client registration
2. The server maintains a response cache that is updated per 30 seconds, so even if the instance is just registered it will not appear in the _Eureka_ response immediately
3. _Eureka_ client maintains a cache of registry information. The cache is refreshed per 30 seconds
4. _Ribbon_ also maintains a local cache to avoid calling the client for every request. It may take another 30s.

If you are migrating an existing Spring Cloud based solution to Azure, please make sure your ad-hoc _Eureka_ and _Config Server_ instances are removed (or disabled) to avoid conflict with the managed instances provided by Azure Spring Cloud.

You may also check _Eureka_ client logs in _Azure Log Analytics_. For more details, please visit `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/diagnostic-settings-guide.md`

To get started with _Azure Log Analytics_, please visit https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal. You will need to query the logs by using [Kusto Query Language](https://docs.microsoft.com/azure/kusto/query/).

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Analyze logs and metrics with Diagnostic settings: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/diagnostic-settings-guide.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
