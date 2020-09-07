<properties
pageTitle="Where's my data?"
description="Where's my data?"
infoBubbleText="Some suggestions have been found to help solve your missing data issue quicker."
service="microsoft.insights"
resource="components"
authors="debugthings"
ms.author="jamdavi"
displayOrder=""
articleId="diagnostic-missing-ingestion-data-quotacapped"
diagnosticScenario="ApplicationInsightsMissingDataDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32602225"
resourceTags=""
productPesIds="15693"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Where's my data?

## **Your application has reached its quota**
<!--issueDescription-->
Our diagnostic has detected that the Application Insights resource with name <!--$ComponentName-->[ComponentName]<!--/$ComponentName--> and instrumentation key <!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey--> has reached its daily cap <!--$Time-->[Time]<!--/$Time-->. To fix this you should increase your daily cap.
<!--/issueDescription-->

## **Recommended Steps**

The daily cap is a cost saving tool. Hitting the daily cap is often associated with organic growth of your application traffic. You should review your data to see if this is an expected increase and plan for more data usage. The best option is to increase your daily cap, but you should make sure you understand your data usage before increasing this value as it will increase your cost. If you do not want to increase your costs you should consider sampling.

* [Increase your daily cap](https://docs.microsoft.com/azure/azure-monitor/app/pricing)
* Enable or configure [sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling#ingestion-sampling) to reduce traffic
 

## **Recommended Documents**

* [Manage usage and costs](https://docs.microsoft.com/azure/azure-monitor/app/pricing)<br>
* [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling#ingestion-sampling)<br>
* [Filter telemetry with a Telemetry Processor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#filtering)