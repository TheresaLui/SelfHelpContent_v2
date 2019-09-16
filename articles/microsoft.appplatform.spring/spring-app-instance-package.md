<properties
	pageTitle="Azure Spring Cloud application package cannot be deployed"
	description="Azure Spring Cloud application package cannot be deployed"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	displayOrder="1"
	articleId="spring-app-instance-package"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Azure Spring Cloud application package cannot be deployed

## **Recommended Steps**

* Due to known limitation you cannot upload JAR/source package via Azure portal or ARM template
* When you deploy your application package thought [Azure CLI](https://docs.microsoft.com/cli/azure/), it will be periodically polling the deployment progress, and in the end it shows the deployment result
* If the polling is interrupted, you can still use the following command to fetch the deployment logs: `az asc app show-deploy-log`
* The build logs is also covered if you upload a source package. However, please note that one ASC service instance can only trigger one build job at same time.

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-managed-service-for-spring-cloud-docs/blob/master/README.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-managed-service-for-spring-cloud-docs/blob/master/docs/faq.md`
