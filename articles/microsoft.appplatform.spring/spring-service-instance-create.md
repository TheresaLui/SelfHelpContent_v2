<properties
	pageTitle="Azure Spring Cloud service instance cannot be created"
	description="Azure Spring Cloud service instance cannot be created"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	displayOrder="1"
	articleId="spring-service-instance-create"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Azure Spring Cloud service instance cannot be created

* The name of the Azure Spring Cloud service instance will be used for requesting sub domain name under azureapps.io, so the creation will fail if the name conflicts with an existing one. You may find more details in activity logs.
* The whole creation process might take up to 5 minutes
* When you try to create an Azure Spring Cloud service instance via Azure portal, we will do validation for you
* However, if you try to create the Azure Spring Cloud service instance via [Azure CLI](https://docs.microsoft.com/cli/azure/) or [ARM template](https://docs.microsoft.com/azure/azure-resource-manager/), please verify:

	* The subscription is active
	* The location is supported by Azure Spring Cloud
	* The resource group for the instance is already created
	* The resource name conforms to the naming rule: *It can contain only lowercase letters, numbers and hyphens. The first character must be a letter. The last character must be a letter or number. The value must be between 2 and 32 characters long.*

* If you try to create the ASC service instance via ARM template, check the [ARM template syntax](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-authoring-templates)

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-managed-service-for-spring-cloud-docs/blob/master/README.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-managed-service-for-spring-cloud-docs/blob/master/docs/faq.md`
