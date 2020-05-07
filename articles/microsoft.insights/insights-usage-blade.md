<properties 
    pageTitle="I am having problems with the Application Insights Users, User Flows, Funnels, or other user behavior analytics tools"
    description="General troubleshooting guide for Application Insights Users, User Flows, Funnels, or other user behavior analytics tools."
    infoBubbleText="Some suggestions have been found to help solve your Usage issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="numberbycolors"
    articleId="insights_usage_blade"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32609669"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am having problems with the Application Insights Users, User Flows, Funnels, or other user behavior analytics tools

## **Recommended steps**

1.  Please look through [these common issues and solutions](https://docs.microsoft.com/azure/application-insights/app-insights-usage-troubleshoot) and see if they resolve your issue
2.	Please verify you are using recommended mechanisms of loading the JavaScript SDK, documented here: [Getting Started: Application Insights JavaScript SDK](https://github.com/Microsoft/ApplicationInsights-JS#get-started)
3.	Please verify you have added the Application Insights instrumentation key to the code in your app that initializes Application Insights
4.  Please verify the instrumentation key in the code of your app matches the instrumentation key of the Application Insights resource in which you expect to see data. To see the instrumentation key for an Application Insights resource, go the Overview page of the Application Insights resource in the Azure portal and look in the Essentials section at the top of the page
5.  If you are setting up a new Application Insights resource and are not yet seeing your data appear, wait five minutes, refresh the page, and see if the data appears, then

## Please provide following information to help the team investigate issue

1.	Describe the issues in detail, with the expected behaviors and actual behaviors
2.	What client-side frameworks are used in your application, if any? For example, React or Angular
3.	What is the Application Insights instrumentation key and its resource name?
4.	What is the URL of instrumented site, if issue can be easily reproduced by our team?
5.	What is the Browser version, if the issue seems to be browser-specific?

**Known issues**

* The "Setting the user context in an ITelemetryInitializer" example in the [Send user context documentation](https://docs.microsoft.com/azure/application-insights/app-insights-usage-send-user-context) throws an exception at runtime.

* Auto collection of page duration is not applicable for single page applications. Please use custom [startTrackPage](https://github.com/Microsoft/ApplicationInsights-JS/blob/master/API-reference.md#starttrackpage), [stopTrackPage](https://github.com/Microsoft/ApplicationInsights-JS/blob/master/API-reference.md#stoptrackpage) to instrument scenarios.

**Recommended Documentation**

[Overview of Application Insights user behavior analytics tools](https://docs.microsoft.com/azure/application-insights/app-insights-usage-overview)<br>
[Users, Sessions, and Events](https://docs.microsoft.com/azure/application-insights/app-insights-usage-segmentation)<br>
[Sending and customizing user IDs](https://docs.microsoft.com/azure/application-insights/app-insights-usage-send-user-context)<br>
[User Flows](https://docs.microsoft.com/azure/application-insights/app-insights-usage-flows)<br>
[Funnels](https://docs.microsoft.com/azure/application-insights/usage-funnels)<br>
[Retention](https://docs.microsoft.com/azure/application-insights/app-insights-usage-retention)<br>
[Cohorts](https://docs.microsoft.com/azure/application-insights/app-insights-usage-cohorts)<br>
[Impact](https://docs.microsoft.com/azure/application-insights/app-insights-usage-impact)<br>
[Application Insights JavaScript SDK](https://docs.microsoft.com/azure/application-insights/app-insights-javascript)