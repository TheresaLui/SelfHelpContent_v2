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

* [How to Create Table DDLs to Import into an External Metastore](https://kb.azuredatabricks.net/metastore/create-table-ddl-for-metastore.html)
* [Listing Table Names](https://kb.azuredatabricks.net/metastore/list-tables.html)
* [How to Explore Apache Spark Metrics With Spark Listeners](https://kb.azuredatabricks.net/metrics/explore-spark-metrics.html)


