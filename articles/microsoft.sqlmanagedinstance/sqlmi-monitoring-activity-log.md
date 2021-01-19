<properties
	pageTitle="Activity Log issues with Managed Instance"
	description="Activity Log issues with Managed Instance"
	infoBubbleText="Activity Log issues with Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748861"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-monitoring-activity-log.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Activity Log issues with Managed Instance

The Activity log is a [platform log](https://docs.microsoft.com/azure/azure-monitor/platform/platform-logs-overview) in Azure that provides insight into subscription-level events. This includes such information as when a resource is modified or when a virtual machine is started. You can view the Activity log in the Azure portal or retrieve entries with [PowerShell](https://docs.microsoft.com/powershell/module/az.monitor/get-azlog?view=azps-3.8.0) ([Samples](https://docs.microsoft.com/azure/azure-monitor/samples/powershell-samples#retrieve-activity-log)) and [CLI](https://docs.microsoft.com/cli/azure/monitor/activity-log?view=azure-cli-latest) ([Samples](https://docs.microsoft.com/azure/azure-monitor/samples/cli-samples#view-activity-log)).
 
You can access the Activity log from most menus in the Azure portal. The menu that you open it from determines its initial filter.
For some events, you can view the Change history, which shows what changes happened during that event time, you can see not only that the change, but what was the previous value before the change and what it was changed to.
 
### **Can’t see anything on the Activity Log**
- Try increasing the 'Timespan' to an older moment in time, like 'Last 24 hours' or even older
- Check if there are any other filter that can be filtering out values
- Check if the right subscription, Resource Group and Resource is selected
- The Time stamp of the activities are in UTC+0 by default
 
### **Can't delete or modify the events**
- Entries in the Activity Log are system generated and cannot be changed or deleted.
 
### **When querying the table Azure Activity it doesn't return anything**
- In some cases, the values in these columns may be in all uppercase. If you have a query that includes these columns, you should use the [=~ operator](https://docs.microsoft.com/azure/kusto/query/datatypes-string-operators) to do a case insensitive comparison.

### **Can’t view logs older than 90 days**
- The Activity Log holds the last 90 days of operations.
- If you need to store the Activity Logs for more than 90 day store them in Azure Storage

### **Where can the Activity Log data be stored?**
- [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log#send-to-log-analytics-workspace)
  - To take advantage of Azure Monitor Logs features
  - Send from any single subscription to up to five workspaces. 
  - Collecting logs across tenants requires [Azure Lighthouse](https://docs.microsoft.com/azure/lighthouse/).
  - Activity log is stored in a table called [AzureActivity](https://docs.microsoft.com/azure/azure-monitor/reference/tables/azureactivity) (retrieve with a [log query](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview) in [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal))
- [Azure Event Hubs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log#send-to-azure-event-hubs)
  - Send activity log entries to outside of Azure
  - JSON format
- [Azure Storage](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log#send-to--azure-storage)
  - Retain data for longer than 90 days
  - One JSON blob per hour

### **Using Get-AzLog I can’t get the logs of last month**
- Get-AzLog only provides 15 days of history. 
- Using the **-MaxRecords** parameter allows you to query the last N events, beyond 15 days. 
- To access events older than 15 days, use the REST API or SDK (C# sample using the SDK). If you do not include **StartTime**, then the default value is **EndTime** minus one hour. If you do not include **EndTime**, then the default value is current time. All times are in UTC.

## **Recommended Documents**
- [Azure Monitor Logs](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-logs)
- [REST API](https://docs.microsoft.com/rest/api/monitor/alertrules): [Activity log(s)](https://docs.microsoft.com/rest/api/monitor/activitylogs), [Activity log tenant events](https://docs.microsoft.com/rest/api/monitor/tenantactivitylogs), [(Activity log) event categories](https://docs.microsoft.com/rest/api/monitor/eventcategories) and [Activity log profiles](https://docs.microsoft.com/rest/api/monitor/logprofiles)
- [Azure Monitor partner integrations](https://docs.microsoft.com/azure/azure-monitor/platform/partners)
