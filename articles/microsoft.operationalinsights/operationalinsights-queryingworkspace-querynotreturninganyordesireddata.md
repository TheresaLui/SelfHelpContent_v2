
<properties
pageTitle="Query not returning any or desired data"
description="Query not returning any or desired data"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="noakup"
ms.author="noakuper"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612517"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	articleId="aa9bbb0f-9466-4d77-af8f-314497c4f007"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Query not returning any or desired data

Need help writing or fixing a query? Post your question on the [Log Analytics community space](https://techcommunity.microsoft.com/t5/azure-log-analytics/bd-p/AzureLogAnalytics) for quick answers by the Azure Monitor product group and community.

If your query is valid but does not return the log records you expect, try the following troubleshooting steps:

## **Recommended Steps** 

* Data source configuration: is the data source actually sending the relevant logs to Log Analytics? [Review the required configuration](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources).
* Log ingestion: once configured, your data sources ingest logs to Log Analytics continually. While this process is relatively short, it may take a while during the initial ingestion, when tables are being generated and populated for the first time. **Note**: Only logs created from that point forward will be sent to Log Analytics.
* Log retention: your retention plan sets the time period for which logs are available. If, for example, your retention is set to 7 days, logs older than that will be deleted. To review and update your retention settings, open Azure Log Analytics, select your workspace, select "Usage and estimated costs" from the workspace menu, and open "Data volume management".
* Querying a huge data set: when querying an exceptionally large data set, it's important to follow the query language [best practices](https://docs.microsoft.com/azure/kusto/query/best-practices) to keep query execution time reasonable, and get relevant results.
  If you're using the API, try using an async method to avoid hanging your script on long-running queries, or timing out.
* Log Analytics query editor limit: the query editor displays up to unsorted 10,000 log records. This means you may see partial data, and not necessarily the latest records. To get only the latest records, use the *top* operator. For example, to get the latest 10 records from *MyTable*:

   ```MyTable | top 10 by TimeGenerated```

* Time range and time zone issues:
	* Log records are marked with a timestamp in UTC (Universal time). In your queries, make sure to make the proper adaptations between UTC and your local time zone. For example, you may want to create a new column to hold your local time:
	
	```...| extend localtime = TimeGenerated-8h```
	
	* The Log Analytics query editor applies a "last 24 hours" time range by default. You can use the time picker (located next to the *Run* button) to set a different time range. To assure you're seeing the logs you're interested in, apply conditions to filter out irrelevant log records, and append ```| top 10 by TimeGenerated``` (or another number as you prefer) to your query.
	* Drilling into Log Analytics from a dashboard tile or a customer view created through the view designer - if some or all log records are not showing, review the applied time range. If the time range is set to a specific custom range in the past, it may be querying a time period outside your retention limit. Instead, it is recommended that you apply a relative time range (e.g. "Last 24 hours").

## **Recommended Documents**

* [Overview of common data sources](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources)
* [Getting started with queries](https://docs.microsoft.com/azure/log-analytics/query-language/get-started-queries)
* [Writing search queries](https://docs.microsoft.com/azure/log-analytics/query-language/search-queries)
* [Online course](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
