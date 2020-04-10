<properties
pageTitle="Where's my data?"
description="Where's my data?"
infoBubbleText="Some suggestions have been found to help solve your missing data issue quicker."
service="microsoft.insights"
resource="components"
authors="debugthings"
ms.author="jamdavi"
displayOrder=""
articleId="diagnostic-missing-ingestion-data-throttled"
diagnosticScenario="ApplicationInsightsMissingDataDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32602225"
resourceTags=""
productPesIds="15693"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Where's my data?

## **Your application was throttled**
<!--issueDescription-->
Our diagnostic has detected that the Application Insights resource with name <!--$ComponentName-->[ComponentName]<!--/$ComponentName--> and instrumentation key <!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey--> was throttled <!--$Time-->[Time]<!--/$Time-->. This is an indication that your application was sending data at a higher rate than allowed by the Application Insights ingestion endpoints.
<!--/issueDescription-->

## **Recommended Steps**

This is not a common scenario to be in and will require you to analyze your data. By default Application Insights allows 32,000 events per second averaged over a one minute interval. You should use the following checklist to help determine why you would have run into this situation.

1. Verify there was no sudden increase to the number of machines in your infrastructure
2. Verify there was no sudden increase to the number of requests served by your application
3. Read over and apply [Telemetry Sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling) if the scenario fits
 

## **Recommended Documents**

* [Application Insights Service Limits](https://docs.microsoft.com/azure/azure-monitor/service-limits#application-insights)<br>
* [Telemetry Sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling)