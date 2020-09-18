<properties 
    pageTitle="Application Insights DevOps Widget"
    description="Common solutions to setting up the DevOps Widget"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights-devopswidget"
    displayOrder="202"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602222"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# I have questions about using the DevOps Widget

## **Recommended Steps**

The [Application Insights DevOps Widget](https://marketplace.visualstudio.com/items?itemName=ms-appinsights.ApplicationInsightsWidgets) is used to display data on your **DevOps dashboard** that is part of you DevOps organization to quickly see Application Insights metrics while tracking your code changes and work items. The widget utilizes an [API key](https://dev.applicationinsights.io/documentation/Authorization/API-key-and-App-ID) to query your application insights instance.

### **Generate the API Key**

1. Follow [this guide](https://dev.applicationinsights.io/documentation/Authorization/API-key-and-App-ID) for detailed instructions
2. Navigate to the API Key menu item for you Application Insights Instance
3. Click on the **Create API Key** icon
4. Select **Read Telemetry** from the check box selections
5. Click **Generate key** button
6. Save this key somewhere as it is only displayed once
7. Save the Application ID, as you'll need this too

### **Installing the widget**

1. Navigate to the widget page in the [DevOps Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-appinsights.ApplicationInsightsWidgets)
2. Click **Get it free**
3. Select the DevOps organization to install the extension to
4. [Create or Add a dashboard](https://docs.microsoft.com/azure/devops/report/dashboards/dashboards?view=azure-devops) in Azure DevOps
5. Add the widget to the dashboard
6. Enter the Application Id and API Key you generated for your application
7. Add metrics and thresholds to the widget

## **Recommended Documents**

* [Widget Documentation](https://marketplace.visualstudio.com/items?itemName=ms-appinsights.ApplicationInsightsWidgets)
* [Install DevOps Extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops)<br>
* [DevOps Dashboard](https://docs.microsoft.com/azure/devops/report/dashboards/dashboards?view=azure-devops)<br>
* [API Key](https://dev.applicationinsights.io/documentation/Authorization/API-key-and-App-ID)
