<properties
  pagetitle="Collect IIS logs into Azure Monitor Logs"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="olegan"
  selfhelptype="Generic"
  supporttopicids="32745412"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,blackforest,fairfax,usnat,ussec,mooncake"
  articleid="a75a43bd-34f6-4238-905e-96c82d9ee16b"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Collect IIS logs into Azure Monitor Logs

To troubleshoot collection of IIS logs by using Log Analytics agent for Windows, review 
[this article](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-iis-logs) for instructions. 

For **agent-specific questions** (deployment and/or operation of the agent), we recommend consulting one of the Agent support topics.

Azure Monitor also supports **collecting IIS logs using Windows Azure Diagnostics Extension (WAD)**. See [this article](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-logs#supported-data-types) for instructions.

## **Recommended Steps**

* How can I collect advanced IIS logs?

Azure Monitor only supports IIS log files stored in W3C format and does not support custom fields or IIS Advanced Logging. It does not collect logs in NCSA or IIS native format.

* My IIS logs appear with a delay

Azure Monitor collects IIS log entries from each agent each time the log timestamp changes. The log is read every 5 minutes. If for any reason IIS doesn't update the timestamp before the rollover time when a new file is created, entries will be collected after the creation of the new file. The frequency of new file creation is controlled by the Log File Rollover Schedule setting for the IIS site, which is once a day by default. If the setting is Hourly, Azure Monitor collects the log each hour. If the setting is Daily, Azure Monitor collects the log every 24 hours. 

**We recommend setting the IIS Log File Rollover Schedule to Hourly.** 


## **Recommended Documents**

* [Collect IIS Logs in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-iis-logs)
