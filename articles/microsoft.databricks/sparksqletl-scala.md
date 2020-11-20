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

# Diagnose and resolve Spark issues with Scala API

 [BulkCopyToSqlDB](https://docs.microsoft.com/azure/azure-sql/database/spark-connector#write-data-using-bulk-insert) function does not work if the target table has calculated columns, resulting in error message similars to: 

  ```
  Calculated columns cannot be modified because it is either a computed column or is the result of a UNION operator.
  ```
 
SQL doesn't allow inserting data into calculated column(s) by design, so it throws this error.

## **Recommended Steps**
  
To work around the issue, you can insert dummy column to the calculated column with empty string or insert to a staging table.

## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [Running C++ Code in Scala](https://docs.microsoft.com/azure/databricks/kb/scala/running-c-plus-plus-code-scala)
* [How to Use Apache Spark Metrics](https://docs.microsoft.com/azure/databricks/kb/metrics/spark-metrics)
* [Drop Tables with Corrupted Metadata from the Metastore](https://docs.microsoft.com/azure/databricks/kb/metastore/drop-table-corruptedmetadata)
