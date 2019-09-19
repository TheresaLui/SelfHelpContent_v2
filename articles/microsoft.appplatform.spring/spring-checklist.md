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
	cloudEnvironments="public"
/>

# Checklist before onboard your Spring application to Azure Spring Cloud

- The application can be run locally with the specified Java runtime version
- The environment config (CPU/RAM/Instances) meets the minimum requirement by the application provider
- The configuration items have expected values. For more details, refer to `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/config-server.md`
- The environment variables have expected values
- The JVM parameters have expected values
- It is recommended to disable/remove embedded _Config Server_ and _Eureka_ service from the application package
- If any Azure resources are to be bound via _Service Binding_, make sure the target resources are up and running. For more details, refer to `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/service-binding.md`.

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
* Azure Spring Cloud Azure Service Binding: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/service-binding.md`
* Azure Spring Cloud Config Server: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/config-server.md`
