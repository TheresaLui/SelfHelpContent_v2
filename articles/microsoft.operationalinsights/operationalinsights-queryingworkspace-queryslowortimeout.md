<properties
pageTitle="Query My query is slow or timing out"
description="My query is slow or timing out"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="meirm"
ms.author="meirm"
displayorder=""
selfHelpType="generic"
supportTopicIds="32727887"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
articleId="operationalinsights-queryingworkspace-queryslowortimeout"
ownershipId="AzureMonitoring_LogAnalytics"
/>
# My query is slow or timing out

## **Recommended Steps** 

### **Examine the query performance profile**

### **Consider applying query optimization steps**

The following article review all the possible explains all the common query performance optimization techniques: https://docs.microsoft.com/azure/azure-monitor/log-query/query-optimization

Most common query optimization tips:

* Don’t use 'contains', use 'has' instead – 'has' is much more efficient than 'contains' on large data sets.

* Consider running the query on shorter time range - The time range of the query has the most substantial influence on the query performance. When less time is scanned, less data is processed.

* Consider using the time range selector in the portal and not specifying it in the query – In some cases, it would cause the system to scan less data.

* Add simple string and scalar filters early in the query – Exclude irrelevant records early in the query processing.

* Avoid JSON and XML parsing when not critical – You can treat them as strings to do early filtering.
