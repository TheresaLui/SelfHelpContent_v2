<properties 
    pageTitle="How do I enable Application Insights for an App Service?"
    description="Explain the current state of App Services integration"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_appservice"
    displayOrder="99"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax"
    productPesIds="15693" 
    supportTopicIds="32602209"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# How do I enable Application Insights for an App Service?

If you're using an App Service with Application Insights there has been a recent change in how the services are integrated. It is recommended (but not required) to remove the existing extension and use the new experience to enable Application Insights. Using the built-in experience will ensure all of the latest settings and versions are applied. Please follow the steps in the Recommended Documents section below.<br>

If you plan to do this, please do so during an appropriate window as it will require a few application recycles and will take your application offline during this process.<br>

## **Recommended Steps**

**To remove the existing extension**<br>

1. Navigate to the App Service
2. Select **Extensions** from the menu
3. Select the **Application Insights** extension
4. Click **Delete**
5. Restart the App Service

**To enable Application Insights**<br>

1. Navigate to the App Service
2. Select Application Insights in the Azure control panel for your app service
3. Specify which resource to use
4. Enable specific features for your platform

## **Recommended Documents**
[Enabling Application Insights in an App Service](https://docs.microsoft.com/azure/azure-monitor/app/azure-web-apps)<br>
[Delete Site Extension API](https://docs.microsoft.com/rest/api/appservice/webapps/deletesiteextension)