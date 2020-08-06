<properties
pageTitle="Where's my data?"
description="Where's my data?"
infoBubbleText="Some suggestions have been found to help solve your missing data issue quicker."
service="microsoft.insights"
resource="components"
authors="debugthings"
ms.author="jamdavi"
displayOrder=""
articleId="diagnostic-sampledtelemetryothersdk"
diagnosticScenario="ApplicationInsightsSampledTelemetryDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32602225"
resourceTags=""
productPesIds="15693"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Where's my data?

## **Telemetry has been sampled**
<!--issueDescription-->
Our diagnostic has detected that the configured application(s) has sampled telemetry in the Application Insights resource with name <!--$ComponentName-->[ComponentName]<!--/$ComponentName--> and instrumentation key <!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey--> <!--$Time-->[Time]<!--/$Time-->. Sampled telemetry might account for your missing data and you should review our sampling resources to see if you need to alter your settings.
<!--/issueDescription-->

## **Recommended Steps**

For non .NET SDK applications you would have had to set sampling explicitly so it's existence is probably expected, however the missing data might not be. Review these queries to see if the missing data is due to a configuration change like an SDK upgrade or due to a traffic change.

**Show what data types have been sampled in the last 24 hours**

This query will show the average sampling percentage over the last 24 hours. This is aggregated and will give you an idea of what types of telemetry is being sampled. 

```
union traces, requests, customEvents, dependencies, exceptions 
| where timestamp >  ago(1h)
| summarize count(), sum(itemCount), percentageretained = (((count() * 1.0 / sum(itemCount) * 1.0) * 100.0)) by itemType 
| where percentageretained < 100.0 | project TelemetryType = itemType, RawRecordCount = count_, ItemCount = sum_itemCount, Percentage = percentageretained
```

**Show what data types have been sampled in the last 24 hours as a chart**

This query will show the average sampling percentage over the last 24 hours per hour per data type. This should give you an idea if you're being sampled more at a specific time. The chart will show a dip if your data has been sampled.

```
union traces, requests, customEvents, dependencies, exceptions 
| where timestamp >  ago(1h)
| summarize count(), sum(itemCount), percentageretained = (((count() * 1.0 / sum(itemCount) * 1.0) * 100.0)) by itemType, bin(timestamp, 1h) 
| project timestamp, itemType, percentageretained
| render timechart
```

## **Recommended Documents**

* [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling#ingestion-sampling)<br>
* [Filter telemetry with a Telemetry Processor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#filtering)