<properties
	pageTitle="Create or Drop Resources/Monitoring, Metrics and Alerts"
	description="Create or Drop Resources/Monitoring, Metrics and Alerts"
	infoBubbleText="Create or Drop Resources/Monitoring, Metrics and Alerts"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637273, 32637274, 32637275"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="cd4cc9ef-4cdb-4e1d-9a81-4f4034395a56"
	ownershipId="AzureData_AzureSQLMI"
/>

# Monitoring - Monitor

Monitoring performance for Managed Instance is supported through built-in metrics in Azure portal, through Azure SQL Analytics, third party tools, and your own implementation of DMV querying.

Please note that QPI (Query Performance Insights), metrics alerting from Azure Portal, and Automatic tuning index management is not supported for Managed Instance at this time. In addition, monitoring with SCOM is not supported for monitoring Managed Instance at this time.

## **Recommended Steps**

To monitor performance of Managed Instance, consider using one of the following options available:

1. Monitor Managed Instance performance using [Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql):

	* Monitor Managed Instance through Azure SQL Analytics. To configure, see [Configure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#configuration). Note that the setup is a multiple-step process involving the following:
		* Add SQL Analytics solution from marketplace and configure it.
		* Configure Diagnostic Settings for each Managed Instance you wish to monitor (this will enable streaming of instance telemetry to SQL Analytics). 
		* Configure Diagnostic Settings for each instance database you wish to monitor (this will enable streaming of database telemetry to SQL Analytics).

	* Consider setting up Intelligent Insights that can help automatically troubleshoot some of the most [common performance issues](https://docs.microsoft.com/azure/sql-database/sql-database-intelligent-insights-troubleshoot-performance#detectable-database-performance-patterns) along with SQL Analytics.
		* You will need to have SQL Analytics configured as a prerequisite
		* Enable streaming of SQL Insights log using [Diagnostics settings](https://docs.microsoft.com/azure/sql-database/sql-database-metrics-diag-logging#configure-streaming-of-diagnostics-telemetry-for-instance-databases) for each database monitored to enable Intelligent Insights

2. Monitor Managed Instance performance real-time:

	* Consider building own solution using open-source Grafana, see [Real-time performance monitoring for Azure SQL Database Managed Instance](https://techcommunity.microsoft.com/t5/DataCAT/Real-time-performance-monitoring-for-Azure-SQL-Database-Managed/ba-p/305537)

3. Monitor Managed Instance through Azure Portal:

	* Select managed instance in the portal and CPU and Storage utilization will be shown on the overview blade.
	* Click on the CPU graph to customize and configure monitoring for IOPS and storage.

4. Build your own solution using DMV querying:

	* You can schedule your own queries using the built-in Agent.
	* Note that DBA knowledge is required for this option.

5. Consider using third party products that support Managed Instance.

## **Recommended Documents**

* [Monitor Azure SQL Database using Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
* [Setup alerting on Azure SQL Database Managed instance using log queries](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#creating-alerts-for-managed-instance)
* [Get started with Azure Monitor log queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-queries)
