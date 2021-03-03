
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

Need help writing or fixing a query? Post your question on the [Log Analytics community space](https://techcommunity.microsoft.com/t5/azure-log-analytics/bd-p/AzureLogAnalytics) for quick answers by the Azure Monitor product group and community.

### **Use Example queries**

Getting started with queries is easiest through the examples provided in the portal. 
On the resource or workspace Logs page you can find the *Example queries* menu, located at the top right area. 
Pick a query to see its text in the query editor, where you can adjust it to your needs.

### **Query by table**
   
All ingested logs are organized by tables, that you can easily query. A list of all tables can be found on the left area of the Logs page, titled *Tables*. To query a table, you can either:
- Hover on a table in the Tables list and click the Preview icon
- Type the name of the table into the query editor, and click Run. For example, to review the Perf table, type:
   
   ```Perf```

To learn how to filter logs, search for a term, sort, extend and more, see [Getting started with queries](https://docs.microsoft.com/azure/log-analytics/query-language/get-started-queries).

### **Can't find your data?**

If your query is valid but doesn't return the expected results, consider the following:

* Sorting - Logs are not sorted by default. That means you may not see the latest records on top. To get the latest records, use the *top* operator, for example:
  ```SecurityEvent | top 10 by TimeGenerated```
* Time range - The query editor applies a default "last 24 hours" time range. You can use the time picker (located next to the *Run* button) to set a different time range.
* Capping - The query editor displays up to 10,000 records. If you've reached the 10K limit, apply filters to narrow down the result set.
* Ingestion - The logs ingestion process is relatively quick, but the initial ingestion may take a while, as tables are being generated and populated for the first time.

## **Recommended Documents**

* [Writing search queries](https://docs.microsoft.com/azure/log-analytics/query-language/search-queries)
* [Query examples](https://docs.microsoft.com/azure/log-analytics/query-language/examples)
* [Online course](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
