<properties
  pagetitle="Log data appears with delay&#xD;"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="olegan,shemers"
  selfhelptype="Generic"
  supporttopicids="32745411"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake,blackforest"
  articleid="05738708-090b-4494-8935-c4827de74c53"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Log data appears with delay

The typical delay to ingest log data is between 2 to 5 minutes. The specific latency for any particular data will vary depending on a variety of factors. [Learn more about data ingestion time](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time).

Typical issues that cause ingestion delay are:
* Service incidents - These are rare, but they happen and may affect one or many data types.
* Data type is inherently slow - Some data types are slow. Frequently this relates to how data is being collected.
* Customer-side delays - Some VMs introduce additional delays. These can occur due to network issues.

## **Recommended Steps**

* Review the **[Azure Monitor Status blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)** for service availability and issues. If you see a notification about an ongoing incident, we are working on it and will communicate through the same blog when it's resolved.

* Check for recent latency issues by running the following Log Analytics query:

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

  
**Note:** You can customize thresholds in the above query or run it on any table

   This query displays 20 VMs with the highest ingestion latency. Examine the results in the **RESULT** column: **OK** means the latency is within normal; **SERVICE DELAY** indicates that the delay is on the Log Analytics service side; **AGENT DELAY** signals some latency before the data reaches the Log Analytics ingestion endpoint.

   For additional insights, consult this [article](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#factors-affecting-latency).

* Check if your resource is sending the data. Run the following query to list the active computers that haven’t recently reported a heartbeat (heartbeat is sent once a minute):

```
Heartbeat  
| where TimeGenerated > ago(1d) //show only VMs that were active in the last day 
| summarize NoHeartbeatPeriod = now() - max(TimeGenerated) by Computer  
| top 20 by NoHeartbeatPeriod desc
```

* Check if the issue is related to a **new custom log table**. When a new type of custom data is created from a custom log or the Data Collector API, the system creates a dedicated storage container. This is a one-time overhead that occurs only on the first appearance of this data type. It may take 10-15 for new custom log table to be made available, however, this does not affect the ingestion - your data will be safely stored into the table  

* Review [this article for additional queries to investigate the latency](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#checking-ingestion-time)


## **Recommended Documents**

* [Log data ingestion time in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time)
* [Azure Monitor Status blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)<br>
