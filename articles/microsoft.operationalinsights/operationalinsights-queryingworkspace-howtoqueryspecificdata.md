
<properties
pageTitle="How to query specific data"
description="How to query specific data"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="noakup"
ms.author="noakuper"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612464"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	articleId="78a1e1e4-038e-474b-a9b1-f24d9ca0d41a"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# How to query specific data

Querying data can be done in two ways: directly querying a specific table, or searching through your entire set of data. The first approach is preferable, since it's scoped to a relevant data source and therefore more efficient.

### **Querying a specific table**

If you know the name of the relevant table, querying it is simple:

* **Everything in a specific table**
   
To review all log records in a table, write the name of the table:
   
   ```Perf```
   
This query returns everything in the *Perf* table, which holds performance-related logs.
   
* **Get the latest logs**
   
To get the latest records, use the *top* operator. For example:
   
```SecurityEvent | top 10 by TimeGenerated```
   
This query returns the latest 10 records logged in the *SecurityEvent* table.
   
* **Filter records**
   
To review only logs that match a given condition, use the *where* operator:<br/>
   
``` SecurityEvent | where Level == 8```
   
This query returns only records in which the Level column holds the value 8.
   
* **Search for a term**
   
To search for a term across all columns of a table for an interesting term, use *search*:<br/>
   
``` search in (Event) "timeout"```
   
This query searches the *Event* table for any record that contains the term "timeout".

### **Searching through your data set**

If you don't know which table to query or intentionally want to query across all tables, you can run an open search query:
   
``` search "error"```
   
The query returns every log records the contains the term "error".
   
This type of query may be easier to start with if you're not familiar with the schema of tables, but is less recommended since it may take a longer time to run, and may return too many results.

### **Can't find your data?**

If your query is valid but it does not return the log records you expect, consider the following:

* By default, the Log Analytics query editor applies a "last 24 hours" time range. You can use the time picker (located next to the *Run* button) to set a different time range.
* The Log Analytics query editor displays up to 10,000 log records, unsorted. This means you may see partial data, and not necessarily the latest records. To assure you're seeing the latest records, apply conditions to filter out irrelevant log records, and use the *top* operator as shown in the example above.
* Logs are being ingested to Log Analytics all the time. While this process is relatively short, it may take a while during the initial ingestion, when tables are being generated and populated for the first time.

## **Recommended Documents**

* [Getting started with queries](https://docs.microsoft.com/azure/log-analytics/query-language/get-started-queries)
* [Writing search queries](https://docs.microsoft.com/azure/log-analytics/query-language/search-queries)
* [Query examples](https://docs.microsoft.com/azure/log-analytics/query-language/examples)
* [Online course](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
* [Log Analytics community space](https://aka.ms/AzureLogAnalyticsCommunity)
