
<properties
pageTitle="My query returns with error "
description="Deflection article for queries returning with errors"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="roygal"
ms.author="roygal"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612514"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
articleId="b53c5697-02b1-4956-8198-cf0520f3024a"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Query Samples

Queries may return with errors in a few cases, the Log Analytics UI should provide an error message to point you at the right direction.
i.	There’s an issue with the query syntax – queries may return an  error if not composed correctly:
1.	Use our example queries to get a head start on building a query ‘right’: https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/examples
2.	Refer to the following documentation for writing a query: https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-queries
3.	Refer to the following documentation for improving queries and building efficient queries: https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/query-optimization
4.	Refer to the following KQL guide to learn more about KQL – Log analytics querying language: https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/query-language
ii.	There’s an issue with underlying log analytics configuration – underlying  Log Analytics configuration may result in queries returning unexpected results or errors:
1.	Check your workspace  configuration – is everything configured correctly? See the following article for pointers:
https://docs.microsoft.com/en-us/azure/azure-monitor/platform/design-logs-deployment
2.	Check permissions – are your permissions configured correctly? 
Read the following articles to behitter understand Log Analytics permissions:
https://docs.microsoft.com/en-us/azure/azure-monitor/platform/roles-permissions-security
3.	https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-access
iii.	There’s an issue with the Log Analytics service – The Log Analytics service might be experiencing issues or undergoing maintenance in your area.
Please refer to the Azure Status to get Log Analytics service status:
https://status.azure.com/en-us/status 
If the Log Analytics service is undergoing maintenance or experiencing issues, please try running your query at a later time. 


Many query samples are available through Log Analytics itself:

1. Basic examples are available when you open a new tab, or open the *Help* menu, and select *Examples*
2. Additional query examples and solution queries are available through the Query Explorer

Additional examples are available in the documentation articles listed below. You can also use the Log Analytics [demo environment](https://portal.loganalytics.io/demo#) to try out any of these examples on real data.

## **Recommended Documents**

* [Query examples](https://docs.microsoft.com/azure/log-analytics/query-language/examples)
* [Performance counters](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-performance-counters?toc=/azure/azure-monitor/toc.json#log-searches-with-performance-records)
* [Windows events](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-windows-events?toc=/azure/azure-monitor/toc.json#log-searches-with-windows-events)
* [Syslog](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-syslog?toc=/azure/azure-monitor/toc.json#log-queries-with-syslog-records)
* [IIS logs](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-performance-counters?toc=/azure/azure-monitor/toc.json#log-searches-with-performance-records)
* [Log Analytics query language reference](https://docs.microsoft.com/azure/log-analytics/query-language/query-language)
* [Online course](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
* [Log Analytics community space](https://aka.ms/AzureLogAnalyticsCommunity)

