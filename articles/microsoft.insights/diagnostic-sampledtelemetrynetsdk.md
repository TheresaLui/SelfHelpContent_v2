<properties
pageTitle="Where's my data?"
description="Where's my data?"
infoBubbleText="Some suggestions have been found to help solve your missing data issue quicker."
service="microsoft.insights"
resource="components"
authors="debugthings"
ms.author="jamdavi"
displayOrder=""
articleId="diagnostic-sampledtelemetrynetsdk"
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

By default all .NET SDK implementations will have sampling enabled to reduce costs. To start investigating what is being sampled, follow some of these suggestions:

1. Look for changes to your application traffic
2. Investigate the times and amount of sampling using these queries below
3. Review the [Configuring adaptive sampling for ASP.NET applications](https://docs.microsoft.com/azure/azure-monitor/app/sampling#configuring-adaptive-sampling-for-aspnet-applications) document for ways to tune your sampling amounts

**Tips for reducing the occurrence of sampling**

1. Increase **MaxTelemetryItemsPerSecond** in the sampling configuration
2. Remove a specific type of telemetry from being sampled by adding it to the **ExcludedTypes** in the sampling configuration
3. Look for the largest amount of data generated (dependencies for example) and decide if you should filter out some of these using a [Telemetry Processor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#filtering)


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