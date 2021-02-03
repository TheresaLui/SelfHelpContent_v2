<properties
  pagetitle="Monitoring - Monitor, Metrics, and Alerts"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="katmac"
  selfhelptype="Generic"
  supporttopicids="32637273"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="09add851-4125-406c-af6a-70eff2d8d7e1"
  ownershipid="AzureData_AzureSQLMI" />
# Monitoring - Monitor, Metrics, and Alerts

**Monitoring** for Microsoft Azure SQL Managed Instance is supported through built-in metrics within the Microsoft Azure portal, through Azure SQL Analytics, third party tools, and your own implementation of DMV querying.

**Please note that SQL Managed Instance is not supported on Query Performance Insights (QPI), metrics alerting from the Azure portal, and Azure SQL DB Automatic Index Tuning at this time. In addition, monitoring Managed Instance is not supported using System Center Operations Manager (SCOM) at this time.**

**Alert** can be configured on metric values for SQL Managed Instance. Alerts can send you an email, call a web hook, run Azure Functions, runbook, call an external ITSM compatible ticketing system, call you on the phone or send a text message when some metric, for example instance storage size or CPU usage, reaches a predefined threshold. 
 
## **Recommended Steps**

To monitor metrics of SQL Managed Instance, consider using one of the following options available:

**Monitor SQL Managed Instance Through Azure Portal**

1. Select SQL Managed Instance in the portal. The CPU and Storage utilization will be shown on the Overview pane.
1. Click the CPU graph to customize and configure monitoring for IOPS and storage. Note that metrics in the Azure portal are reported at the instance level. If you want to monitor database level resource usage, follow the instructions below to build your own solution.
 
To configure, see [Configure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#configuration). Note that the setup is a multiple-step process requiring you to:

- Add the SQL Analytics solution from the Microsoft Azure Marketplace and configure it
- Configure Diagnostic Settings for each managed instance you want to monitor. This enables streaming of instance telemetry and database telemetry to SQL Analytics.

Optionally, set up Intelligent Insights to help automatically troubleshoot some of the more [common performance issues](https://docs.microsoft.com/azure/sql-database/sql-database-intelligent-insights-troubleshoot-performance#detectable-database-performance-patterns). Before you can set up Intelligent Insights, you will need to:

- Configure SQL Analytics first
- Use [Diagnostic Settings](https://docs.microsoft.com/azure/sql-database/sql-database-metrics-diag-logging#configure-streaming-of-diagnostics-telemetry-for-instance-databases) to enable streaming of the SQL Insights log for each database you want to monitor

**Monitor Managed Instance Performance Real-Time**

- Consider building your own solution using open-source Grafana, see [Monitoring options available for Azure SQL Managed Instance](https://techcommunity.microsoft.com/t5/azure-sql-database/monitoring-options-available-for-azure-sql-managed-instance/ba-p/1065416).
- Monitor SQL Managed Instance performance using [Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql). This feature is currently in Public Preview. 

**Build Your Own Solution Using DMV Querying**

- Schedule your own queries using the built-in agent
- Use the database mail feature in SQL Managed Instance to send email notifications automatically upon the DMV query result. Note that database administrator knowledge is required for this option.

**Use a Third-Party Product that Supports SQL Managed Instance**

-  Consider using a third-party tool that supports SQL Managed Instance for your monitoring requirements

**Set Up Alerts for SQL Managed Instance**

- To configure alerts for SQL Managed Instance, see [Create Alert for SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create)

## **Recommended Documents**

* [Monitoring options available for Azure SQL Managed Instance](https://techcommunity.microsoft.com/t5/azure-sql-database/monitoring-options-available-for-azure-sql-managed-instance/ba-p/1065416)
* [Monitor Azure SQL Database using Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
* [Get started with Azure Monitor log queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-queries)
* [Monitoring Microsoft Azure SQL Database and Azure SQL Managed Instance performance using dynamic management views](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#monitor-resource-use)
* [Configure Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/configure-database-mail)