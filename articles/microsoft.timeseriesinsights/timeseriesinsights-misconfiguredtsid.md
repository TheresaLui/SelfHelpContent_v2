<properties
  pagetitle="Environment configuration issue due to misconfigured Time Series ID property"
  service="microsoft.timeseriesinsights"
  resource="environments"
  ms.author="lyhughes"
  selfhelptype="Resource"
  supporttopicids="32571148"
  resourcetags=""
  productpesids="16244"
  cloudenvironments="public,mooncake,fairfax,usnat,ussec"
  articleid="timeseriesinsights-misconfiguredtsid"
  ownershipid="AzureIot_IotTSI" />
# Environment configuration issue due to misconfigured Time Series ID property

When an environment's Time Series ID (TS ID) is misconfigured or missing from an event, "(null)" will appear in the Explorer in place of your time series instances. This occurs when the TS ID provided at environment creation time is not present in your JSON telemetry payload. 

## **Recommended Steps** 

1. Check the Time Series ID for your environment on the overview page
2. Make sure that the value provided is the correct unique identifier for your time series instances, and that it is present as a JSON property in your telemetry event payload
3. If you have a complex JSON payload, refer to the ingestion [rules](https://docs.microsoft.com/azure/time-series-insights/concepts-json-flattening-escaping-rules) to understand how your JSON will be flattened and stored. Your TS ID should match the column name in storage after flattening.
4. An environment Time Series ID is immutable and cannot be changed. If it is incorrect, make a new Azure Time Series Insights environment.

## **Recommended Documents**

* [Best practices for choosing a Time Series ID](https://docs.microsoft.com/azure/time-series-insights/time-series-insights-update-how-to-id)
* [JSON Flattening, Escaping, and Array Handling](https://docs.microsoft.com/azure/time-series-insights/concepts-json-flattening-escaping-rules)