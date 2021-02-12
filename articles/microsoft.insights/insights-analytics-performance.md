<properties 
    pageTitle="I am having performance problems with my Analytics Queries"
    description="Will help assist with query errors and performance."
    infoBubbleText="Some suggestions have been found to help solve your performance issues quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="noakuper"
    articleId="insights_analytics_performance"
    displayOrder="92"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602201"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am having performance problems with my Analytics Queries

**Analytics Queries Performance & Failures**<br>

Querying and analyzing application log data can cover a very wide scope. It is therefore important to understand the best practices to use, and what might affect your query's performance, or even fail it.<br>

Queries can be done in two ways: directly querying a specific table (such as *requests*), or searching through your entire set of data. The first approach is preferred since it's scoped to a relevant data source and therefore more efficient.

## **Recommended Steps**

**General Performance Issues**<br>

* **Scope your query**: Querying a wider scope than you actually need may lead to a long-running query, and often result in too many (irrelevant) records in your result set. In some cases, the query may even time out and fail.
* **Select the relevant data source**: The first step in writing an efficient query is focusing on the relevant data source, which usually means selecting the table to query
* **Specifying a table** is always preferred over running an wide text search (such as **search \***)
* **Set the relevant time range**: By default, your query will cover the last 24 hours. If you're interested in log records from the last hour, select that option in the Time Range selector (located next to the *Run* button) or add it explicitly to your query. It is best to add the time filter immediately after the table name, ex. **requests | where timestamp > ago(1h)**
* **Get only the latest logs**: To review only the latest records, use the *top* operator. ex,  **traces | top 10 by timestamp**
* **Filter records**: To review only logs that match a given condition, use the *where* operator, ex. **traces | where severityLevel > 0**
   
**Improve your query performance**<br>

* **Using has vs contains**: When evaluating strings, prefer **has** over **contains** when looking for full tokens. **has** is more performant as it doesn't have to look-up for substrings.
* **Use project** to narrow the set of columns being processed to only those you need: **traces | project timestamp, severityLevel, client_City | ...**
* **Use extend** to calculate values and create your own columns, always prefer to filter on a table column, ex. **customEvents | extend subscription = split(operation_Name, "/")[2] | where subscription == "acb"**
* **Using joins** When using the **join** operator - choose the table with less rows to be the first one (left-most).

**Query failures**<br>

Almost all query failures are caused by syntax errors, rather than connection failures etc. Here are the most common errors:

**No query statement found**<br>

This very common "syntax error" actually means you didn't select a query before clicking the *Run* button (or using the Shift+Enter shortcut). Simply make sure your cursor is on the relevant query and run it again.<br>

**Failed to resolve table / column / scalar expression named ...**<br>

This common error is usually just a typo - your query refers to a table, column or other expression using a wrong name. For example, instead of typing: **requests | where timestamp > ago(1h)** you might have typed: **request | where timestamp > ago(1h)** To fix this error, simply review the query and look for a red squiggly line - it marks the text that was probably misspelled.

**Missing closing brackets or quotation marks**<br>

These common typing errors result in a "Syntax error" or "query could not be parsed at '<EOF>'" message.<br>

**Handling special characters**<br>

If your query contains special characters, you will need to escape them or use **@** to create a verbatim string literal. Read more about it [here](https://docs.microsoft.com/azure/kusto/query/scalar-data-types/string).<br>

## **Recommended Documents**

* [Getting started with queries](https://docs.microsoft.com/azure/log-analytics/query-language/get-started-queries)<br>
* [Writing search queries](https://docs.microsoft.com/azure/log-analytics/query-language/search-queries)<br>
* [Query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices)<br>
* [Query language online course](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
