<properties
	pageTitle="Portal and Client Tools/Azure SQL Analytics"
	description="Portal and Client Tools/Azure SQL Analytics"
	infoBubbleText="Portal and Client Tools/Azure SQL Analytics"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637241"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="4059fca6-fa08-4be5-8d9f-b31b92652f7b"
	ownershipId="AzureData_AzureSQLMI"
/>

# Monitor Managed Instance performance with SQL Analytics

Azure SQL Analytics is an advanced cloud monitoring solution for monitoring performance of Azure SQL Databases, elastic pools, and Managed Instances at scale and across multiple subscriptions through a single pane of glass. It collects and visualizes important Azure SQL Database performance metrics with built-in intelligence for performance troubleshooting.

## **Recommended Steps**

### Configure Azure SQL Analytics with Managed Instance

To monitor performance of Managed Instance using Azure SQL Analytics, follow these steps:

1. To configure Azure SQL Analytics, follow steps described in [Configure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#configuration). Note that the setup is a multiple-step process involving the following:

* Add SQL Analytics solution from marketplace and configure it.
* Configure Diagnostic Settings for each Managed Instance you wish to monitor (this will enable streaming of instance telemetry to SQL Analytics). 
* Configure Diagnostic Settings for each instance database you wish to monitor (this will enable streaming of database telemetry to SQL Analytics).

2. Consider setting up Intelligent Insights that can help automatically troubleshoot some of the most [common performance issues](https://docs.microsoft.com/azure/sql-database/sql-database-intelligent-insights-troubleshoot-performance#detectable-database-performance-patterns).
* You will need to have SQL Analytics configured as a prerequisite
* Enable streaming of SQLInsights log using [Diagnostics settings](https://docs.microsoft.com/azure/sql-database/sql-database-metrics-diag-logging#configure-streaming-of-diagnostics-telemetry-for-instance-databases) for each database monitored to enable Intelligent Insights

### Troubleshooting issues with Azure SQL Analytics:

* Cannot see a database in SQL Analytics:
  * Ensure database has some meaningful workload. Idle databases will not be shown in SQL Analytics. Databases configured for monitoring with SQL Analytics must have some workload on them in order for the monitoring telemetry to start flowing from database into the solution.
  * If you are sure there exists workload on a database and monitoring data is not showing up in SQL Analytics in more than 30 minutes after being configured, consider removing [Diagnostics settings](https://docs.microsoft.com/azure/sql-database/sql-database-metrics-diag-logging#configure-streaming-of-diagnostics-telemetry-for-instance-databases) for each database not shown, and then re-enabling. This will re-trigger registration of a database for monitoring.

* Telemetry is lagging:
  * By design it is expected that telemetry is lagging behind for up to 10 minutes for Azure SQL Database Managed Instance.
  * For real-time monitoring needs, consider setting up own solution using open-source Grafana, see [Real-time performance monitoring for Azure SQL Database Managed Instance](https://techcommunity.microsoft.com/t5/DataCAT/Real-time-performance-monitoring-for-Azure-SQL-Database-Managed/ba-p/305537)

### Setup alerting through SQL Azure Analytics:

* Alerts can be created on all monitored telemetry through SQL Analytics. This is achieved through writing a query on data that is triggered upon condition being meet. See [examples of queries](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#creating-alerts-for-managed-instance) to setup alerting through SQL Analytics.

* For writing additional queries use [Azure Monitor log queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-queries).

## **Recommended Documents**

* [Monitor Azure SQL Database using Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
* [Setup alerting on Azure SQL Database Managed instance using log queries](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#creating-alerts-for-managed-instance)
* [Get started with Azure Monitor log queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-queries)