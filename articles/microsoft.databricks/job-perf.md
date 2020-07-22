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
 
## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [How to Resolve Job Hangs and Collect Diagnostic Information](https://docs.microsoft.com/azure/databricks/kb/jobs/job-hang-resolve-and-collect-diagnostics)
