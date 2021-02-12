<properties
	pageTitle="Checklist before onboard your Spring application to Azure Spring Cloud"
	description="Checklist before onboard your Spring application to Azure Spring Cloud"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-checklist"
	displayOrder="9"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# Checklist before onboard your Spring application to Azure Spring Cloud

- The application can be run locally with the specified Java runtime version
- The environment config (CPU/RAM/Instances) meets the application provider's minimum requirements
- The configuration items have expected values. For more information about Azure Spring Cloud Config Server, refer to [Tutorial: Use Config Server to maintain application configuration](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-tutorial-config-server)
- The environment variables have expected values
- The JVM parameters have expected values
- It is recommended to disable/remove embedded _Config Server_ and _Eureka_ services from the application package
- When binding Azure services via _Service Binding_, ensure the target resources are up and running.

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [Tutorial: Use Config Server to maintain application configuration](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-tutorial-config-server)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
