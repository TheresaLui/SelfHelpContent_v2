<properties
	pageTitle="How do I know which event in my input data is causing issue?"
	description="How do I know which event in my input data is causing issue?"
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="SnehaGunda"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>


# How do I know which event in my input data is causing issue?

## **Recommended steps**

1. When the input stream of your Stream Analytics job contains incorrect serialization such as missing parenthesis in a JSON object, incorrect time stamp format, it causes serialization issues. When a Stream Analytics job receives such malformed messages, it drops the message and notifies user with a warning. A warning symbol is shown on the Inputs tile of your Stream Analytics job.
2. Navigate to the input blade and click to view warnings.
3. The input details blade displays a set of warnings with details about the issue, you can view the Stream Analytics documentation [troubleshooting document](https://docs.azure.cn/stream-analytics/stream-analytics-malformed-events) for an example.
4. To get the JSON data that has incorrect format, run a c# code block to read the partition Id, offset and output the data at that offset. You can get the full sample from our [GitHub samples repository](https://github.com/Azure/azure-stream-analytics/blob/master/Samples/CheckMalformedEventsEH/GetMalformedEvents.cs). Once you read the data, you can analyze and correct the serialization format.

## **Recommended documents**

* [Detailed troubleshooting with example screen shots](https://docs.azure.cn/stream-analytics/stream-analytics-malformed-events)<br>
* [GitHub samples repository](https://github.com/Azure/azure-stream-analytics/blob/master/Samples/CheckMalformedEventsEH/GetMalformedEvents.cs)
