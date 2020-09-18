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

# Diagnose and resolve issues with DBFS mount point

## **Recommended Steps**

* **Problem:**
  
  [BulkCopyToSqlDB](https://docs.microsoft.com/azure/azure-sql/database/spark-connector#write-data-using-bulk-insert) function does not work if the target table has calculated columns getting error message similar to: 

  ```
  Calculated columns cannot be modified because it is either a computed column or is the result of a UNION operator.
  ```
  **Cause:** 
  
  As SQL doesn't allow inserting data into calculated column(s) by design, it throws this error.

  **Solution:**
  
  To workaround the issue, you can insert dummy column to the calculated column with empty string or insert to a staging table.
  
## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [How to Create Table DDLs to Import into an External Metastore](https://docs.microsoft.com/azure/databricks/kb/metastore/create-table-ddl-for-metastore)
* [Listing Table Names](https://docs.microsoft.com/azure/databricks/kb/metastore/list-tables)
* [How to Explore Apache Spark Metrics With Spark Listeners](https://docs.microsoft.com/azure/databricks/kb/metrics/explore-spark-metrics)


