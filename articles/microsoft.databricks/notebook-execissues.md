<properties
	pageTitle="Diagnose and resolve execution issues"
	description="Diagnose and resolve execution issues"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677690"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="635b660f-911e-4568-aab6-82ca7126648b"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve execution issues

## **Recommended Steps**

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform

* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.

* Getting error **java.io.EOFException** when handling huge data set in Spark R even with larger cluster - issue is caused by design since Spark R uses driver node specific framework resource. Resolution is to handle the pipeline with dividing data into smaller sets and conquer the results.

* Getting exception **py4j.security.Py4JSecurityException: … is not whitelisted** on High Concurrency cluster with Credential Passthrough enabled - this exception is thrown when you have accessed a method that Azure Databricks has not explicitly marked as safe for Azure Data Lake Storage credential passthrough clusters. In most cases, this means that the method could allow a user on a Azure Data Lake Storage credential passthrough cluster to access another user’s credentials. To resolve issue:
    - You can either disable Credential Passthrough for this HC cluster
    - Or use Standard cluster with Credential Passthrough enabled where single user access is allowed

* The cluster returns **Cancelled** in a Python notebook
     * Follow this KB article to troubleshoot and resolve issue: [Cluster cancels Python command execution due to library conflict](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)
     
* Getting error **Remote RPC client disassociated. Likely due to containers exceeding thresholds, or network issues.** - We generally get RPC error due to the following reasons:

  1. The communication between the driver and executor is lost - executor is not able to send heartbeats within the threshold time frame which can happen either if the executor is overwhelmed with memory/OOM errors or too many network hits are making executor too busy in GC and it is not able to respond back to driver.

     You could see what is happening in the Spark UI > Stages > sort the tasks based on the error. It will show you what error was happening on executor level.

     One quick workaround would be to use bigger cluster (if current cluster is really small).

  2. Having too many partitions - small files can cause RPC error. You can check the used partition strategy.

  3. Running multiple notebooks on the same cluster can sometimes cause issues on the driver. If that is the case, split the workload across multiple clusters.
     
## **Recommended Documents**

* How to connect to data sources from Azure Databricks:
     * [Azure SQL database](https://docs.microsoft.com/azure/databricks/data/data-sources/sql-databases)
     * [Azure Data Lake Storage](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2)
     * [Azure Blob Storage](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-storage)
     * [Azure Cosmos DB](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/cosmosdb-connector)
     * [Azure Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-spark-connector)
     * [Azure SQL Data Warehouse](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/)
* [Troubleshooting Unresponsive Python Notebooks or Canceled Commands](https://docs.microsoft.com/azure/databricks/kb/notebooks/troubleshoot-cancel-command)
* Python library conflicts can result in cancelled commands. The Azure Databricks support organization sees conflicts most often with versions of ipython, numpy, scipy, and pandas : [Troubleshooting Steps](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#python-command-cancelled) 
* [Common Errors in Notebooks](https://docs.microsoft.com/azure/databricks/kb/notebooks/common-errors-in-notebooks)
* [Cannot Run Notebook Commands After Canceling Streaming Cell](https://docs.microsoft.com/azure/databricks/kb/notebooks/streaming-notebook-stuck)

* To [increase quota limits](https://docs.microsoft.com/azure/azure-supportability/per-vm-quota-requests), please follow the steps:

    * Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
    * Select the subscription that needs an increased quota
    * Select Usage + quotas
    * In the upper right corner, select Request increase
    * Fill in the forms for the type of quota you need to increase
    
* Databricks **Performance Tuning**:
	* [Azure Databricks Best Practices](https://github.com/Azure/AzureDatabricksBestPractices/blob/master/toc.md)
	* [Optimizing Apache Spark SQL Joins](https://databricks.com/session/optimizing-apache-spark-sql-joins)
	* [Correctness and Performance of Apache Spark SQL](https://databricks.com/session/a-framework-for-evaluating-the-performance-and-the-correctness-of-the-spark-sql-engine)
	* [Delta Engine Optimization](https://docs.microsoft.com/azure/databricks/delta/optimizations/)
