<properties
	pageTitle="Debug ASA query"
	description="Debug ASA query"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-troubleshootdiaglogs"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628777"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Debug ASA Query

Queries in Azure Stream Analytics are expressed in an SQL-like query language. The query design can express simple passthrough logic to move event data from one input stream into another output data store, or it can do rich pattern matching and temporal analysis to calculate aggregates over time.

Stream Analytics also supports JavaScript and C# user-defined functions which can be invoked directly from your query. You can develop and test your C# UDFs in Visual Studio and your JavaScript UDFs can be tested using any browser.

To learn more, see the recommended documents.

## **Recommended Documents**

* [Easily debug query logic with live data in Visual Studio](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-live-data-local-testing)
* [Common query patterns](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-stream-analytics-query-patterns)
* [Debugging ASA query logic](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-query)
