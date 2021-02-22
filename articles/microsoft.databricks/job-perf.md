<properties
	pageTitle="Diagnose and resolve issues with job performance"
	description="Diagnose and resolve issues with job performance"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677703"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ffd3d204-607f-4a47-aee4-8a61f4a03056"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with job performance

* Getting error **Unexpected error while loading Spark UI: Max Response Size Reached**: the issue is due to response limit of 30 MB for Spark UI proxy. This can happen if the jobs page returned by Spark UI is very big which can happen in long running cluster with too many jobs. To resolve the issue, please modify [Spark UI configurations](http://spark.apache.org/docs/latest/configuration.html#spark-ui) as below:

```
    spark.ui.retainedJobs 100
    spark.ui.retainedStages 100
    spark.ui.retainedTasks 10000
 ```
 * To handle transient connection errors it is recommended to
      * Increase the connection timeout setting to 120 seconds
      * Implement retry logic, 2 – 3 minutes between each retry
      
 * Monitoring [Driver node](https://docs.microsoft.com/azure/databricks/clusters/configure#driver-node) performance:
    * [Ganglia metrics](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#ganglia-metrics)
    * [Diagnostic logging in Azure Databricks]( https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/azure-diagnostic-logs) - you can stream the VM's metrics to Azure Log Analytics Workspace by installing the Log Analytics Agent on each cluster node
    **Note:** This could increase cluster startup time by a few minutes
    * [SSH to Driver on VNet injected workspace](https://docs.microsoft.com/azure/databricks/clusters/configure#--ssh-access-to-clusters) and run bash commands

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* Databricks **Performance Tuning**:
	* [Azure Databricks Best Practices](https://github.com/Azure/AzureDatabricksBestPractices/blob/master/toc.md)
	* [Optimizing Apache Spark SQL Joins](https://databricks.com/session/optimizing-apache-spark-sql-joins)
	* [Correctness and Performance of Apache Spark SQL](https://databricks.com/session/a-framework-for-evaluating-the-performance-and-the-correctness-of-the-spark-sql-engine)
	* [Delta Engine Optimization](https://docs.microsoft.com/azure/databricks/delta/optimizations/)
