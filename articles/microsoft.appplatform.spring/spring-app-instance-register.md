<properties
	pageTitle="Azure Spring Cloud application instance cannot be registered"
	description="Azure Spring Cloud application instance cannot be registered"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	displayOrder="1"
	articleId="spring-app-instance-register"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Azure Spring Cloud application instance cannot be registered

## **Recommended Steps**

* If you are migrating an existing Spring Cloud based solution to Azure, please make sure your ad-hoc Eureka and Config Server instances are removed (or disabled) to avoid conflict with the managed instances provided by Azure Spring Cloud
* Wait at least 2 minutes for a newly registered instance start receiving traffic. This is because of few reasons:

1. The first heartbeat happens 30s after startup, this heartbeat is for client registration
2. The server maintains a response cache that is updated per 30s, so even if the instance is just registered it will not appear in the eureka response immediately
3. Eureka client maintains a cache of registry information. The cache is refreshed per 30s.
4. Ribbon also maintains a local cache to avoid calling the client for every request. It may take another 30s.

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-managed-service-for-spring-cloud-docs/blob/master/README.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-managed-service-for-spring-cloud-docs/blob/master/docs/faq.md`
