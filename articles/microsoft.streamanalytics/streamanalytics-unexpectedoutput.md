<properties
	pageTitle="Unexpected output"
	description="Unexpected output"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-unexpectedoutput"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32357244"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public"
	ms.author="sidram"
/>

# Unexpected Output
There are times when your Stream Analytics query may not be producing the output you are expecting. This could happen due to a variety of reasons. If your query uses TIMESTAMP BY, the please be sure to configure event ordering policies according to your latency and correctness requirements. If the event ordering policies look ok, you can also debug and understand why your job is producing unexpected output, see the recommended documents.


## **Recommended Documents**

* [How to configure event ordering policies and how they might impact your output](https://docs.microsoft.com/azure/stream-analytics/event-ordering)
* [Debug queries progressively](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-query#debug-queries-progressively)
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
