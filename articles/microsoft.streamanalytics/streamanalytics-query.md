<properties
	pageTitle="Develop query"
	description="Develop query"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-query"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628770"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Develop Query
Queries in Azure Stream Analytics are expressed in an SQL-like query language. The query design can express simple passthrough logic to move event data from one input stream into another output data store. or it can do rich pattern matching and temporal analysis to calculate aggregates over time. You can join data from multiple inputs to combine streaming events, and do lookups against static reference data to enrich the event values. 

Azure Stream Analytics Query Language is a subset of T-SQL. To ensure your query logic will work as expected, please go through the [query language reference](https://docs.microsoft.com/stream-analytics-query/stream-analytics-query-language-reference). 

To learn more about authoring queries in Azure Stream Analytics jobs, see the recommended documents.


## **Recommended Documents**

* [Commonly used query patterns](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-stream-analytics-query-patterns)
* [Tumbling, Hopping, Sliding, and Session Windows](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-window-functions)
* [Geospatial functions in Stream Analytics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-geospatial-functions)
* [Stream Analytics Query Language Reference](https://docs.microsoft.com/stream-analytics-query/stream-analytics-query-language-reference)
