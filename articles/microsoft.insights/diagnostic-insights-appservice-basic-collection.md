<properties 
    pageTitle="How do I enable Application Insights for an App Service in Recommended Collection level?"
    description="Explain the current state of App Services integration"
    infoBubbleText="Some suggestions have been found to help solve your missing data issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="rajkumar-rangaraj"
    ms.author="rajrang"
    articleId="diagnostic_insights_appservice_basic_collection"
    diagnosticScenario="ApplicationInsightsDefaultModeEnablementDiagnostic"
    displayOrder=""
    selfHelpType="diagnostics"
    cloudEnvironments="public"
    resourceTags=""
    productPesIds="15693" 
    supportTopicIds="32602209"
 />
 
## **How do I enable Application Insights for an App Service in Recommended Collection level?**
<!--issueDescription-->
Our diagnostic has detected that the data has come from following SDK versions <!--$SDKTYPE-->[SDKTYPE]<!--/$SDKTYPE--> for the Application Insights resource with name <!--$ComponentName-->[ComponentName]<!--/$ComponentName--> and instrumentation key <!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey--> <!--$Time-->[Time]<!--/$Time-->. <!--$CountOfBasicModeSDK-->[CountOfBasicModeSDK]<!--/$CountOfBasicModeSDK--> <!--$AppServiceList-->[AppServiceList]<!--/$AppServiceList--> enabled in Basic level. .NET Basic collection level offers essential single-instance APM capabilities. Switching to .NET Recommended collection level provides these additonal capabilities.

* Adds CPU, memory, and I/O usage trends.
* Correlates micro-services across request/dependency boundaries.
Collects usage trends, and enables correlation from availability results to transactions.
Collects exceptions unhandled by the host process.
Improves APM metrics accuracy under load, when sampling is used.
<!--/issueDescription-->

## **Recommended Steps**

**To modify Application Insights for Recommended Collection level**<br>

1. Navigate to the App Service
2. Select Application Insights in the Azure control panel for your app service
3. Toggle Collection level switch from Basic to Recommended

## **Recommended Documents**

* [Enabling Application Insights in an App Service](https://docs.microsoft.com/azure/azure-monitor/app/azure-web-apps)<br>
