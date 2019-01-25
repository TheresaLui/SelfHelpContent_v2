<properties
	pageTitle="Moving a Function App"
	description="Moving a Function App"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,cts-shrahman"
    ms.author="shrahman,jebrook"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32598329"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public"
/>

# Moving a Function App

## **Recommended documents**

Azure Function Apps have the same limitations as Azure App Services when moving the resource across subscriptions or resource groups. See the document below  for more detail:<br>
[Move resource group to new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources).<br>

To move an Azure Function App between the consumption plan and dedicated plan requires a redeployment of the function code to a new function app created in the respective plan. A work item to allow this capability is tracked in the Github issue below:<br>
[How to Migrate from Consumption Plan to App Service Plan (and vice versa)](https://github.com/Azure/Azure-Functions/issues/155).