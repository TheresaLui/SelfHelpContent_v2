<properties 
    pageTitle="I am having problems with my JavaScript SDK data"
    description="General troubleshooting guide for JavaScript SDK."
    infoBubbleText="Some suggestions have been found to help solve your JavaScript SDK issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    articleId="insights_javascriptsdk"
    displayOrder="7"
    selfHelpType="resource"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds="32402633"
 />
 # I am having problems with my JavaScript SDK data
## **Recommended steps**
1.	Please verify you are using recommended mechanisms of loading SDK documented here: [Getting Started]( https://github.com/Microsoft/ApplicationInsights-JS#get-started)
2.	Please verify you have specified the instrumented key for correct application.
3.	Please verify SDK version (released by Application Insights, or using external SDK. Extensions to the SDK published by the community are not supported here. Please check and log issue against relevant github repository). Javascript SDK versions released are documented here: [here][JavaScript SDK Releases](https://github.com/Microsoft/ApplicationInsights-JS/releases) 
4.	Please search through GitHub issues if resolution is already available here: [JavaScript SDK Issues](https://github.com/Microsoft/ApplicationInsights-JS) or is an existing active issue.

## **Please provide following information to help the team investigate issue**
1.	Describe issue in detail with expected behavior and actual behavior.
2.	What kind of framework is used in application development (React, Angular, angular, JavaScript/typescript)
3.	What is the instrumentation key and resource name?
4.	URL of instrumented site if issue can be easily retried in client.
5.	Browser version if issue in specific browser only.

## **Known issues**
1.	Auto collection of page duration is not applicable for single page applications. Please use custom startTrackPage, stopTrackPage to instrument scenarios.
