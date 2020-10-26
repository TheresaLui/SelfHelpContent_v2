<properties
	pageTitle="Metrics issues with Azure SQL Database"
	description="Metrics issues with Azure SQL Database"
	infoBubbleText="Metrics issues with Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32749526"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqldb-monitoring-metrics.md"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve Metrics issues with Azure SQL Database

The Azure Portal enables monitoring of resource metrics for your Azure SQL Database. You can quickly monitor a variety of resource metrics, enabling you to see resource consumption at any given moment.

You can configure diagnostic settings to [stream categories of metrics and resource logs](https://docs.microsoft.com/azure/azure-sql/database/metrics-diagnostic-telemetry-logging-streaming-export-configure?tabs=azure-portal#diagnostic-telemetry-for-export) for single databases, pooled databases, and elastic pools to one of the following Azure resources:
- [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs#collect-to-log-analytics-workspace)
  - Can be consumed by [SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
  - Leverage other Azure Monitor features, such as alerts and visualizations
- [Azure Event Hubs](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs#send-to-azure-event-hubs)
  - Stream logs to third-party logging and telemetry systems
  - Build a custom telemetry and logging platform
  - View service health by streaming data to Power BI
- [Azure Storage](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs#send-to-azure-storage)
  - Store data for longer periods
  - Low cost storage

You can enable and manage metrics and diagnostic telemetry logging by using one of the following methods:
- Azure Portal
- PowerShell
- Azure CLI
- Azure Monitor REST API
- Azure Resource Manager template

## **Recommended Steps**

### There are periods where CPU\IO is reaching 100%, what is causing it?
- Check with [Query Performance Insight](https://docs.microsoft.com/azure/azure-sql/database/query-performance-insight-use) to see if the high resource usage is due to the workload
- You can also use [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/query-store-usage-scenarios?view=sql-server-ver15#identify-and-tune-top-resource-consuming-queries) to identify and tune top resource-consuming queries

### There are periods where DTU is reaching 100%, what is causing it?
1. Confirm what resource (CPU/Data IO/Log IO) is being highly used
2. Check with [Query Performance Insight](https://docs.microsoft.com/azure/azure-sql/database/query-performance-insight-use) to see if the high resource usage is due to the workload
3. You can also use [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/query-store-usage-scenarios?view=sql-server-ver15#identify-and-tune-top-resource-consuming-queries) to identify and tune top resource-consuming queries

### There are periods where eDTU is reaching 100%, what is causing it?
1. On the Azure Portal Elastic Pool blade, you can see the list of databases with the 'Avg eDTU (%)' and 'Peak eDTU (%)'
2. Go to the Azure SQL Database that have the higher avg eDTU value
3. Confirm what resource (CPU/Data IO/Log IO) is being highly used
4. Check with [Query Performance Insight](https://docs.microsoft.com/azure/azure-sql/database/query-performance-insight-use) to see if the high resource usage is due to the workload
5. You can also use [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/query-store-usage-scenarios?view=sql-server-ver15#identify-and-tune-top-resource-consuming-queries) to identify and tune top resource-consuming queries

### Export the metrics to outside of Azure
- The metrics can be [streamed](https://docs.microsoft.com/azure/azure-sql/database/metrics-diagnostic-telemetry-logging-streaming-export-configure?tabs=azure-portal#diagnostic-telemetry-for-export) to Azure Event Hubs and Azure Storage, from where they can be sent outside of Azure
- On the Metrics tab, you can download the metrics presented to Excel. Select **Share** > **Download to Excel**.
- Use [REST API](https://docs.microsoft.com/rest/api/monitor/metrics/list) or [Powershell](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetric?view=azps-4.7.0) to obtain the value of the metric that you want

### Can’t see the metrics graph on Azure Portal
- Confirm that the database is processing enough workload to consume resources
- Workaround: [Monitor Performance using DMVs](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#monitor-resource-use) (for [elastic pools](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-elastic-pool-resource-stats-azure-sql-database?view=azuresqldb-current#examples)), [PowerShell](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetric?view=azps-4.7.0), or [REST API](https://docs.microsoft.com/rest/api/monitor/metrics/list)
- On lower-service tiers, the component responsible for uploading metrics can hit the resource limit and stop uploading metrics. Try scaling to a higher service tier, then scale back to the original service tier.
- Confirm that the resource provider [Microsoft.Insights is registered on your subscription](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot#microsoftinsights-resource-provider-isnt-registered-for-your-subscription)
- The user must be a member of [Monitoring Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader), [monitoring contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor), or have the [Contributor role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) to explore metrics for any resource.
- Validate if the chart was edited and if the [y-axis was locked on a specific boundary](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#lock-boundaries-of-chart-y-axis)

### Can’t see all the data in the graph
- In the Azure Portal, you can query only for 30 days of data on any single chart. This limitation doesn't apply to [log-based metrics](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics#log-based-metrics).  
- Verify that the difference between the start date and the end date in the time picker doesn't exceed the 30-day interval.
- Validate if the chart was edited and the [y-axis was locked on a specific boundary](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#lock-boundaries-of-chart-y-axis)

### "Error retrieving data" message on dashboard
- This problem may happen if your dashboard was created with a metric that was later deprecated and removed from Azure. To verify that this is the case, open the Metrics tab of your resource, and check the available metrics in the metric picker. Update the failing tile by picking an alternative metric for your chart on the dashboard.

### Chart shows dashed line
- Azure metrics charts use a dashed line to indicate that there is a missing value (also known as the _null value_) between two known time grain data points. The dashed line drops down to zero when the metric uses count and sum aggregation. For the average, minimum, or maximum aggregations, the dashed line connects the two nearest known data points.  

The dashed line makes reading of these charts easier. However, if your chart is still unclear, consider viewing your metrics with a different chart type.

### Chart shows unexpected drop in values
- In many cases, the perceived drop in the metric values is a misunderstanding of the data shown on the chart. You can be misled by a drop in sums or counts when the chart shows the most-recent minutes because the last metric data points haven’t been received or processed by Azure yet.

## **Recommended Documents**

- [Platform metrics: Databases](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported#microsoftsqlserversdatabases)
- [Platform metrics: Elastic pools](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported#microsoftsqlserverselasticpools)
- [Platform metrics: Managed Instances](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported#microsoftsqlmanagedinstances)
- [Azure Monitoring REST API walkthrough](https://docs.microsoft.com/azure/azure-monitor/platform/rest-api-walkthrough)
- [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)
- [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)
- [Video - Azure SQL Analytics](https://youtu.be/j-NDkN4GIzg)
