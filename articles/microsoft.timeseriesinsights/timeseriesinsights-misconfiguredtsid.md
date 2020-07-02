<properties
	pageTitle="Environment configuration issue due to misconfigured Time Series ID property"
	description="Misconfigured TS ID"
	infoBubbleText=""
	service="microsoft.timeseriesinsights"
	resource="timeseriesinsights"
	ms.author="lyhughes"
	displayOrder="0"
	articleId="timeseriesinsights-misconfiguredtsid"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32571145"
	resourceTags=""
	productPesIds="16244"
	cloudEnvironments="public, mooncake"
	ownershipId="AzureIot_IotTSI"
/>

# Environment configuration issue due to misconfigured Time Series ID property

When an environment's Time Series ID (TS ID) is misconfigured or missing, "(null)" will appear in the Explorer in place of your time series instances or signals. This occurs when the TS ID provided at environment creation time is not present in your JSON telemetry payload.

## **Recommended Steps**

1. Check the Time Series ID for your environment on the overview page
2. Make sure that the value provided is the correct unique identifier for your time series instances, and that it is present in your incoming JSON telemetry payload
3. An environment Time Series ID is immutable and cannot be changed. If it is incorrect, make a new Azure Time Series Insights environment.

## **Recommended Documents**

* [Best practices for choosing a Time Series ID](https://docs.microsoft.com/azure/time-series-insights/time-series-insights-update-how-to-id)
