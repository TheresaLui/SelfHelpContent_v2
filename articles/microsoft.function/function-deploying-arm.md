<properties
	pageTitle="Deploying Function Apps/ARM Templates"
	description="Deploying Function Apps/ARM Templates"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,Jebrook"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32630462"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="63fc3d1c-ebc2-4927-8b22-fd720b4737c5"
	ownershipId="Compute_AppService"
/>

# Deploying Function Apps/ARM Templates

Azure Functions supports automated deployments from ARM templates. The overall layout is similar to deploying an Azure Web app. The main difference is that app settings, specifically AzureWebJobsStorage and AzureWebJobsDashboard, must be in the site configuration property of the function app resource. For example:

```
"properties": {
	"serverfarmId": ""
	"siteConfig": {
		"appSettings": [
		{
			"name": "AzureWebJobsDashboard",
			"value": "StorageConnectionStringValue"
		},
		{
			"name": ""AzureWebJobsStorage",
			"value": "StorageConnectionStringValue"
		},
		…..
}
```

## **Recommended Documents**

* [Using ARM with Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-infrastructure-as-code)<br>



