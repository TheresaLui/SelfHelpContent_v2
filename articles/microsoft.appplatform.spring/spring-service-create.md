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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# I encountered a problem in creating Azure Spring Cloud service instance

The name of the Azure Spring Cloud service instance will be used for requesting a subdomain name under `azureapps.io`, so the provision will fail if the name conflicts with an existing one. You may find more details in the activity logs.

When you try to provision an Azure Spring Cloud service instance via the portal, Azure will validate the request for you.

However, if you try to provision the Azure Spring Cloud service instance via [Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli) or [ARM template](https://docs.microsoft.com/azure/azure-resource-manager/), please verify:

1. The subscription is active
2. The location is supported by Azure Spring Cloud
3. The resource group for the instance is already created
4. The resource name conforms to Azure naming standards. It can contain only lowercase letters, numbers and hyphens. The first character must be a letter. The last character must be a letter or number. The name must be between 2 and 32 characters long.

If you try to create the Azure Spring Cloud service instance via ARM template, check the [ARM template syntax](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-authoring-templates).

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
