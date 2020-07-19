<properties 
    pageTitle="Unsupported SDKs"
    description="Explain the current unsupported SDKs and where to get support"
    infoBubbleText="Your application has unsupported SDKs "
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="diagnostic-unsupportedsdk"
    displayOrder="90"
    diagnosticScenario="ApplicationInsightsUnsupportedSDKDiagnostic"
    selfHelpType="diagnostics"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32402637"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# **Unsupported SDK(s) found in Telemetry**
<!--issueDescription-->
Our diagnostic has detected that the Application Insights resource with name **<!--$ComponentName-->[ComponentName]<!--/$ComponentName-->** and instrumentation key **<!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey-->** **<!--$Time-->[Time]<!--/$Time-->** is sending data using an unsupported SDK. Please see below for details and where to go to get help.
<!--/issueDescription-->

**We have detected the following SDKs in your resource:**

<!--$SDKTYPES-->[SDKTYPES]<!--/$SDKTYPES-->

## **Recommended Steps**

* If you're using an unsupported SDK and the problem is with display of data or incorrect properties, you will need to open an issue in the repository to the respective project
* Please review our up to date list of [supported languages, frameworks, and platforms](https://docs.microsoft.com/azure/azure-monitor/app/platforms)

