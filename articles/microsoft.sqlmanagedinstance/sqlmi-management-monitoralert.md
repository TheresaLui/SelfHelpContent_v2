<properties
	pageTitle="Management and Monitoring|Monitoring, Metrics, Alert"
	description="Management and Monitoring|Monitoring, Metrics, Alert"
	service="microsoft.sql"
	resource="servers"
	authors="zhizhwan"
    ms.author="zhizhwan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637273"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="09add851-4125-406c-af6a-70eff2d8d7e1"
	ownershipId="AzureData_AzureSQLMI"
/>

# Monitoring - Monitor, Metrics, Alert
**Monitoring** for Managed Instance is supported through built-in metrics in Azure portal, through Azure SQL Analytics, third party tools, and your own implementation of DMV querying.

**Please note that QPI (Query Performance Insights), metrics alerting from Azure Portal, and Automatic tuning index management is not supported for Managed Instance at this time. In addition, monitoring with SCOM is not supported for monitoring Managed Instance at this time.**


**Alert** can be configured on metric values for SQL Managed Instance. Alerts can send you an email, call a web hook, execute Azure Function, runbook, call an external ITSM compatible ticketing system, call you on the phone or send a text message when some metric, such is for example instance storage size, or CPU usage, reaches a predefined threshold. 


## **Recommended Steps**

To monitor metrics of Managed Instance, consider using one of the following options available:

1. Monitor Managed Instance through Azure Portal:

	* Select managed instance in the portal and CPU and Storage utilization will be shown on the overview blade 
	* Click on the CPU graph to customize and configure monitoring for IOPS and storage
    * Note that metrics in Azure Portal are instance level. If you want to monitor database level resource usage, please jump to option 4 to build your own solution.

2. Monitor Managed Instance performance using [Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql):

	* Monitor Managed Instance through Azure SQL Analytics. To configure, see [Configure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#configuration). Note that the setup is a multiple-step process involving the following:
		* Add SQL Analytics solution from marketplace and configure it
		* Configure Diagnostic Settings for each Managed Instance you wish to monitor (this will enable streaming of instance telemetry to SQL Analytics)
		* Configure Diagnostic Settings for each instance database you wish to monitor (this will enable streaming of database telemetry to SQL Analytics)

	* Consider setting up Intelligent Insights that can help automatically troubleshoot some of the most [common performance issues](https://docs.microsoft.com/azure/sql-database/sql-database-intelligent-insights-troubleshoot-performance#detectable-database-performance-patterns) along with SQL Analytics
		* You will need to have SQL Analytics configured as a prerequisite
		* Enable streaming of SQL Insights log using [Diagnostics settings](https://docs.microsoft.com/azure/sql-database/sql-database-metrics-diag-logging#configure-streaming-of-diagnostics-telemetry-for-instance-databases) for each database monitored to enable Intelligent Insights

3. Monitor Managed Instance performance real-time:

	* Consider building own solution using open-source Grafana, see [Real-time performance monitoring for Azure SQL Database Managed Instance](https://techcommunity.microsoft.com/t5/DataCAT/Real-time-performance-monitoring-for-Azure-SQL-Database-Managed/ba-p/305537)


4. Build your own solution using DMV querying:

	* You can schedule your own queries using the built-in Agent
    * You can use database mail feature in Managed Instance to send email notifications automatically upon the DMV query result
    * Note that DBA knowledge is required for this option

5. Consider using third party products that support Managed Instance

To configure alert for Managed Instance, see [Create Alert for SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create). 

## **Recommended Documents**

* [Monitor Azure SQL Database using Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
* [Get started with Azure Monitor log queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-queries)
* [Monitoring Microsoft Azure SQL Database and Azure SQL Managed Instance performance using dynamic management views](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#monitor-resource-use)
* [Configure Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/configure-database-mail)
