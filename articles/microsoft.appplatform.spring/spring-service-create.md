<properties
	pageTitle="I encountered a problem in creating Azure Spring Cloud service instance"
	description="I encountered a problem in creating Azure Spring Cloud service instance"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-service-create"
	displayOrder="4"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I encountered a problem in creating Azure Spring Cloud service instance

The name of the Azure Spring Cloud service instance will be used for requesting a subdomain name under `azureapps.io`, so the provision will fail if the name conflicts with an existing one. You may find more details in the activity logs.

When you try to provision an Azure Spring Cloud service instance via the portal, it will do validation for you.

However, if you try to provision the Azure Spring Cloud service instance via [Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli) or [ARM template](https://docs.microsoft.com/azure/azure-resource-manager/), please verify:

1. The subscription is active
2. The location is supported by Azure Spring Cloud
3. The resource group for the instance is already created
4. The resource name conforms to the naming rule

   _It can contain only lowercase letters, numbers and hyphens. The first character must be a letter. The last character must be a letter or number. The value must be between 2 and 32 characters long._

If you try to create the Azure Spring Cloud service instance via ARM template, check the [ARM template syntax](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-authoring-templates).

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
