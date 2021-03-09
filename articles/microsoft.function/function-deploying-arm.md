<properties
  pagetitle="Deploying Function Apps/ARM Templates"
  description="Deploying Function Apps/ARM Templates"
  service="microsoft.web"
  resource="sites"
  ms.author="Jebrook,shrahman"
  selfhelptype="Generic"
  supporttopicids="32630462"
  resourcetags=""
  productpesids="16072"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="63fc3d1c-ebc2-4927-8b22-fd720b4737c5"
  ownershipid="Compute_AppService" />
# Deploying Function Apps/ARM Templates

## **Recommended Steps**

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

Note: 
WEBSITE_RUN_FROM_PACKAGE setting should be made consistent between ARM template and Deployment task to avoid unexpected issues around file updates when deploying. For example, if using Run From Package in the DevOps deployment task, make sure the ARM template also uses  WEBSITE_RUN_FROM_PACKAGE = 1, and if not using Run From Package in the DevOps deployment task, make sure the ARM template uses  WEBSITE_RUN_FROM_PACKAGE = 0 (or omits this setting.

## **Recommended Documents**

* [Using ARM with Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-infrastructure-as-code)
* [ARM Dependency Guidance](https://docs.microsoft.com/azure/app-service/deploy-resource-manager-template)
* [Using Functions Private Endpoints with AzureWebJobsStorage](https://github.com/mcollier/azure-functions-private-storage)