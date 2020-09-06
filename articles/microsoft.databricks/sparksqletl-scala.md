<properties
	pageTitle="Diagnose and resolve issues with Scala"
	description="Diagnose and resolve issues with Scala"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677727"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c6b918f1-6292-4714-b2bf-eceb3ad29d0b"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Scala

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

* [Running C++ Code in Scala](https://kb.azuredatabricks.net/scala/running-c-plus-plus-code-scala.html)
* [How to Use Apache Spark Metrics](https://kb.azuredatabricks.net/metrics/spark-metrics.html)
* [Drop Tables with Corrupted Metadata from the Metastore](https://kb.azuredatabricks.net/metastore/drop-table-corruptedmetadata.html)

