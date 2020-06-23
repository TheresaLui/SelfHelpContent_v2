
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

# **My query returns with error**

Queries may return with errors in a few cases, the Log Analytics UI should provide an error message to point you at the right direction.

1. There’s an issue with the query syntax
    Queries may return an  error if not composed correctly:
    1.	Use our [example queries](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/examples) to get a head start on building a query ‘right’.
    2.	Refer to the following [documentation for writing a query](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-queries).
    3.	Refer to the following [documentation for improving queries and building efficient queries](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/query-optimization).
    4.	Refer to the following [KQL guide](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/query-language) to learn more about KQL – Log analytics querying language.
2. 	There’s an issue with underlying log analytics configuration
    Underlying Log Analytics configuration may result in queries returning unexpected results or errors:
    1.	Check your workspace configuration – is everything configured correctly? See the [following article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/design-logs-deployment)for pointers.
    2.	Check permissions – are your permissions configured correctly? 
        Read the following articles to [better understand Log Analytics permissions](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/roles-permissions-security) and to [manage Log Analytics access](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-access).
3. There’s an issue with the Log Analytics service
    The Log Analytics service might be experiencing issues or undergoing maintenance in your area.
    Please refer to the [Azure Status page](https://status.azure.com/en-us/status) to get Log Analytics service status.
    If the Log Analytics service is undergoing maintenance or experiencing issues, please try running your query at a later time. 

## **Recommended Documents**

* [Query examples](https://docs.microsoft.com/azure/log-analytics/query-language/examples)
* [Performance counters](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-performance-counters?toc=/azure/azure-monitor/toc.json#log-searches-with-performance-records)
* [Windows events](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-windows-events?toc=/azure/azure-monitor/toc.json#log-searches-with-windows-events)
* [Syslog](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-syslog?toc=/azure/azure-monitor/toc.json#log-queries-with-syslog-records)
* [IIS logs](https://docs.microsoft.com/azure/log-analytics/log-analytics-data-sources-performance-counters?toc=/azure/azure-monitor/toc.json#log-searches-with-performance-records)
* [Log Analytics query language reference](https://docs.microsoft.com/azure/log-analytics/query-language/query-language)
* [Online course](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
* [Log Analytics community space](https://aka.ms/AzureLogAnalyticsCommunity)

