
<properties
pageTitle="Log data appears with delay"
description="Log data appears with delay"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="05738708-090b-4494-8935-c4827de74c53"
symptomID=""
infoBubbleText=""
authors="olegan, yossiy"
ms.author="olegan"
displayorder=""
selfHelpType="generic"
supportTopicIds="32745411"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Log data appears with delay

The typical delay to ingest log data is between 2 and 5 minutes. The specific latency for any particular data will vary depending on a variety of factors. Please consult this [article](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time) for the detailed guidance.

Typical issues causing ingestion delay are:
* Service incidents - these are rare, but they happen. They may affect one or many types
* Data type is inherently slow - some data types are slow. Frequently it relates to how data is being collected.
* Customer-side delays - sometime, some VMs may introduce additional delays. This may occur due to some network issues 

## **Recommended Steps**

* Review the **[Azure Monitor Status blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)** for service availability and issues. If you are seeing a notification about ongoing incident - we are already working on it and will communicate through the same blog once it is resolved.

* Check for recent **latency issues** - execute the following Log Analytics query:

```
Heartbeat
| where TimeGenerated > ago(8h) 
| extend E2EIngestionLatency = ingestion_time() - TimeGenerated 
| extend AgentLatency = _TimeReceived - TimeGenerated 
| summarize percentiles(E2EIngestionLatency, 95), percentiles(AgentLatency, 95) by Computer
| extend RESULT=iff(percentile_E2EIngestionLatency_95 < 5min, "OK", 
		    iff(percentile_AgentLatency_95 > 2min, "AGENT DELAY", "SERVICE DELAY"))
| top 20 by percentile_E2EIngestionLatency_95 desc
```

*Note: you can customize thresholds in the above query or run it on any table*

This query displays 20 VMs with highest ingestion latency. Examine the results (RESULT column) - OK means the latency is within normal, SERVICE DELAY indicates delay on Log Analytics service side, AGENT delay signals some latency before the data reaches Log Analytics ingestion endpoint.

Consult this [article](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#factors-affecting-latency) for additional insights.

* Check if **your resource is sending the data**. Use the following query to list the active computers that haven’t reported heartbeat recently (heartbeat is sent once a minute)

```
Heartbeat  
| where TimeGenerated > ago(1d) //show only VMs that were active in the last day 
| summarize NoHeartbeatPeriod = now() - max(TimeGenerated) by Computer  
| top 20 by NoHeartbeatPeriod desc
```

* Check if the issue is related to a **new custom log table**. When a new type of custom data is created from a custom log or the Data Collector API, the system creates a dedicated storage container. This is a one-time overhead that occurs only on the first appearance of this data type. It may take 10-15 for new custom log table to be made available, however, this does not affect the ingestion - your data will be safely stored into the table  

* Check **additional queries** to investigate  the latency, see [this article](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#checking-ingestion-time)

## **Recommended Documents**

* [Log data ingestion time in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time)
* [Azure Monitor Status blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)<br>
