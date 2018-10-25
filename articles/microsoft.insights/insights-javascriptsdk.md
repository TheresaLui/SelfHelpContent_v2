<properties 
    pageTitle="I am having problems with my JavaScript SDK data"
    description="General troubleshooting guide for JavaScript SDK."
    infoBubbleText="Some suggestions have been found to help solve your JavaScript SDK issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="jpiyali"
    articleId="insights_javascriptsdk"
    displayOrder="7"
    selfHelpType="generic"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds="32402633"
 />
# I am having problems with my JavaScript SDK data

## **Recommended steps**

1.	Please verify you are using recommended mechanisms of loading SDK documented here: [Getting Started]( https://github.com/Microsoft/ApplicationInsights-JS#get-started)
2.	Please verify you have specified the instrumented key for correct application
3.	Please verify SDK version (released by Application Insights or using external SDK. Extensions to the SDK published by the community are not supported here. Please check and log issue against relevant github repository). Javascript SDK versions released are documented here: [JavaScript SDK Releases](https://github.com/Microsoft/ApplicationInsights-JS/releases) 
4.	Please search through GitHub issues if resolution is already available here: [JavaScript SDK Issues](https://github.com/Microsoft/ApplicationInsights-JS/issues) or is an existing active issue

**Please provide following information to help the team investigate issue**

1.	Describe issue in detail with expected behavior and actual behavior
2.	What kind of framework is used in application development (React, Angular, angular, JavaScript/typescript)
3.	What is the instrumentation key and resource name?
4.	URL of instrumented site if issue can be easily retried in client
5.	Browser version if issue in specific browser only

**Known issues**

Auto collection of page duration is not applicable for single page applications. Please use custom [startTrackPage](https://github.com/Microsoft/ApplicationInsights-JS/blob/master/API-reference.md#starttrackpage), [stopTrackPage](https://github.com/Microsoft/ApplicationInsights-JS/blob/master/API-reference.md#stoptrackpage) to instrument scenarios.

## **Recommended Documents**
[Getting Started](https://docs.microsoft.com/azure/application-insights/app-insights-javascript)<br>
[JavaScript SDK GitHub](https://github.com/Microsoft/ApplicationInsights-JS/issues)<br>
[Angular Application Example](https://blogs.msdn.microsoft.com/premier_developer/2017/05/11/add-application-insights-to-an-angular-spa/)