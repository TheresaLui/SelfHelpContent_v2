<properties
	pageTitle="Metrics issues with Managed Instance"
	description="Metrics issues with Managed Instance"
	infoBubbleText="Metrics issues with Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748863"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-monitoring-metrics.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Metrics issues with Managed Instance

The Azure portal enables monitoring of resource metrics for your Managed Instance. You can quickly monitor a variety of resource metrics, enabling you to see resource consumption at any given moment.

You can configure diagnostic settings to [stream categories of metrics and resource logs](https://docs.microsoft.com/azure/azure-sql/database/metrics-diagnostic-telemetry-logging-streaming-export-configure?tabs=azure-portal#diagnostic-telemetry-for-export) for managed instances to one of the following Azure resources.
- [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs#collect-to-log-analytics-workspace)
  - Can be consumed by [SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
  - Leverage other Azure Monitor features such as alerts and visualizations
- [Azure Event Hubs](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs#send-to-azure-event-hubs)
  - Stream logs to third-party logging and telemetry systems
  - Build a custom telemetry and logging platform
  - View service health by streaming data to Power BI
- [Azure Storage](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs#send-to-azure-storage)
  - Store data for longer periods
  - Low cost storage

You can enable and manage metrics and diagnostic telemetry logging by using one of the following methods:
- Azure portal
- PowerShell
- Azure CLI
- Azure Monitor REST API
- Azure Resource Manager template

### There are periods where CPU\IO is reaching 100%, what is causing it?
- You can also use [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/query-store-usage-scenarios?view=sql-server-ver15#identify-and-tune-top-resource-consuming-queries) to identify and tune top resource consuming queries
- Try [Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql) to see if the high resource usage is due to the workload



## **Recommended Documents**
- Platform metrics: [Databases](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported#microsoftsqlserversdatabases)
- Platform metrics: [Elastic pools](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported#microsoftsqlserverselasticpools)
- Platform metrics: [Managed Instances](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported#microsoftsqlmanagedinstances)
- [Azure Monitoring REST API walkthrough](https://docs.microsoft.com/azure/azure-monitor/platform/rest-api-walkthrough)
- [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)
- [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)
- Video - [Performance Monitoring for Azure SQL Managed Instance with Azure SQL Analytics](https://www.youtube.com/watch?v=ESBxcoR3DyA) ([Previous video about Azure SQL Analytics](https://youtu.be/j-NDkN4GIzg))
