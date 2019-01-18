<properties
	pageTitle="Deploying Function Apps/Visual Studio"
	description="Deploying Function Apps/Visual Studio"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,jebrook"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32630472"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public"
/>

# Deploying Function Apps/Visual Studio

## **Recommended steps**

When deploying Azure Functions from Visual Studio, make sure the function runs locally using the latest Azure Function Runtime Core Tools. The Azure Function Runtime, targeting versions 1.x or 2.x, is updated periodically.<br> 
[Announcements regarding Function Runtime releases to the platform](https://github.com/Azure/app-service-announcements/issues)<br>

App settings, such as connection strings for bindings, are not automatically updated on your function app located in the cloud. Validate that these settings are present under the Azure Portal -> Function App -> Application Settings. If these settings are missing or incorrect, your function app may behave unexpectedly or the function app may return an error "Function Host is currently unavailable". If [application insights](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#query-telemetry-data) is enabled, host start up errors and exceptions can be investigated. Please see the documentation linked below on handling application settings with Visual Studio Deployments for more detail.<br>
[Handling App Settings with Visual Studio Deployments](https://docs.microsoft.com/azure/azure-functions/functions-develop-vs#function-app-settings)<br>

If you are deploying to an existing Function App that already has code deployed, a deployment from Visual Studio will automatically overwrite the existing code. If this is running under the dedicated plan you can restore the previous code using the feature located [here](https://docs.microsoft.com/azure/app-service/app-service-web-restore-snapshots). If this is running under the consumption plan, the code is hosted on customer maintained Azure Files Storage account, where the App Services infrastructure does not create backups of this resource. You can disable the overwrite setting in visual studio under the deployment options of the Publishing Wizard.<br>

For other general questions about using Visual Studio with Azure Functions please see the Deploying from Visual Studio document linked below.<br> 
[Deploying from Visual Studio](https://docs.microsoft.com/azure/azure-functions/functions-develop-vs#publish-to-azure)


