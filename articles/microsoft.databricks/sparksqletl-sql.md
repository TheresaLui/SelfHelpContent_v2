<properties
	pageTitle="Diagnose and resolve issues with SQL"
	description="Diagnose and resolve issues with SQL"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32681393"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d9141b4d-3574-45a4-aded-bab8b56c746e"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with SparkSQL API

## **Recommended Steps**

* **Problem:** [BulkCopyToSqlDB](https://docs.microsoft.com/azure/azure-sql/database/spark-connector#write-data-using-bulk-insert) function does not work if the target table has calculated columns, resulting in an error message similar to: 
  ```
  Calculated columns cannot be modified because it is either a computed column or is the result of a UNION operator.
  ```
   **Cause:** SQL doesn't allow inserting data into calculated column(s) by design, it throws this error.  
   **Solution:** To work around the issue, you can insert dummy column to the calculated column with empty string or insert to a staging table.


* **Problem:** You get the following error message in the SQL Statement:
  ```
  Calculated columns cannot be modified because it is either a computed column or is the result of a UNION operator.
  ```
   **Cause:** `spark.databricks.queryWatchdog.outputRatioThreshold` is taking effect. The query is trying fetch or read entire data from source and the data seems to be huge. This includes queries that generate too many output rows, fetch many external partitions, or compute on extremely large datasets. These queries can be extremely slow, saturate cluster resources, and make it difficult for others to share the same cluster.  
   **Solution:** You may close this config in your specific notebook by using the following command. Also, you can improve your cluster configuration for better performance. To do this, see  [Handling large queries in interactive workflows](https://docs.microsoft.com/azure/databricks/spark/latest/spark-sql/query-watchdog).
  ```
  %scala
  spark.conf.set("spark.databricks.queryWatchdog.enabled",false)
  ```
* **Problem:** You are attempting to join two large tables, projecting selected columns from the first table and all columns from the second table. You get error message similar to:
  ```
  org.apache.spark.sql.execution.OutOfMemorySparkException: Size of broadcasted table far exceeds estimates and exceeds limit of spark.driver.maxResultSize=1073741824. You can disable broadcasts for this query using set spark.sql.autoBroadcastJoinThreshold=-1
  ```
   **Cause:** This is due to a limitation with Spark’s size estimator.  
   **Solution:** Follow the [solution here](https://docs.microsoft.com/azure/databricks/kb/sql/bchashjoin-exceeds-bcjointhreshold-oom#solution) to resolve this issue.
 
 * **Problem:** You are using JDBC to write to a SQL table that has primary key constraints, and the job fails with error `PrimaryKeyViolation`  
   **Solution:** Follow the [steps here](https://docs.microsoft.com/azure/databricks/kb/sql/jdbc-write-fails-primarykeyviolation#solution) to resolve this issue.
  
## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [How to Create Table DDLs to Import into an External Metastore](https://docs.microsoft.com/azure/databricks/kb/metastore/create-table-ddl-for-metastore)
* [Listing Table Names](https://docs.microsoft.com/azure/databricks/kb/metastore/list-tables)
* [How to Explore Apache Spark Metrics With Spark Listeners](https://docs.microsoft.com/azure/databricks/kb/metrics/explore-spark-metrics)

