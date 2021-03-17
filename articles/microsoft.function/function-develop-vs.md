<properties
  pagetitle="Developing Functions/Visual Studio&#xD;"
  description="Developing Functions/Visual Studio"
  service="microsoft.web"
  resource="sites"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32742786"
  resourcetags=""
  productpesids="16072"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec,blackforest"
  disableclouds=""
  articleid="60a8fd9a-1bf6-47bf-907d-76b2819f477b"
  ownershipid="Compute_AppService" />
# Developing Functions/Visual Studio

## **Recommended Steps**
1. When deploying Azure Functions from Visual Studio, make sure that the function runs locally using the latest Azure Function Runtime Core Tools. The Azure Function Runtime, targeting versions 1.x or 2.x, is updated periodically.

2. App settings, such as connection strings for bindings, are not automatically updated on your function app located in the cloud. Validate that these settings are present under the Azure Portal > **Function App** > **Application Settings**. 
- If these settings are missing or incorrect, your function app may behave unexpectedly or the function app may return an error "Function Host is currently unavailable". 
- If application insights is enabled, host startup errors and exceptions can be investigated. See the Recommended Documents for more detail on handling application settings with Visual Studio Deployments.

3. If you're deploying to an existing Function App that already has code deployed, a deployment from Visual Studio will automatically overwrite the existing code. 
- If this is running under the dedicated plan, you can restore the previous code using the feature located here. 
- If this is running under the consumption plan, the code is hosted on customer maintained Azure Files Storage account, where the App Services infrastructure does not create backups of this resource. You can disable the overwrite setting in visual studio under the deployment options of the Publishing Wizard.

### Common deployment errors
* When attempting to deploy an Azure Function from Visual Studio:<br>
   ERROR_DESTINATION_INVALID <br>
   "Deployment task failed. ( Could not connect to the remote computer ("*.scm.azurewebsites.net").<br>
  error: The remote name could not be resolved: '.scm.azurewebsites.net'. Publish failed to deploy."<br>

   **Solution:** The Azure Function was deleted from the portal and no longer exists. To resolve, create a New Profile, which recreates the Azure Function App, and then republish the Azure Function.

* When attempting to deploy an Azure Function from Visual Studio while the Azure Function is running.<br>
   ERROR_FILE_IN_USE <br>
   "Error: Web deployment task failed. (Web Deploy cannot modify the file '.dll' on the destination because it is locked by an external process. In order to allow the publish operation to succeed, you may need to either restart your application to release the lock, or use the AppOffline rule handler for .Net applications on your next publish attempt.<br>

   **Solution:** Stop the Azure Function prior to deployment.
    Once Slots for Azure Functions are out of preview, we recommend that you deploy to a slot and then swap.

## **Recommended Documents**
* [Storage Considerations for Functions](https://docs.microsoft.com/azure/azure-functions/storage-considerations)
* [Use Visual Studio to create a C# class library-based function that responds to HTTP requests](https://docs.microsoft.com/azure/azure-functions/functions-create-your-first-function-visual-studio)
* [Develop Azure Functions using Visual Studio](https://docs.microsoft.com/azure/azure-functions/functions-develop-vs)
