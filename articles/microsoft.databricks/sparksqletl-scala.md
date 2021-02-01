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

## **Recommended Steps**

* [BulkCopyToSqlDB](https://docs.microsoft.com/azure/azure-sql/database/spark-connector#write-data-using-bulk-insert) function does not work if the target table has calculated columns, resulting in error message similars to: 

  ```
  Calculated columns cannot be modified because it is either a computed column or is the result of a UNION operator.
  ```
 
  SQL doesn't allow inserting data into calculated column(s) by design, so it throws this error.
  
  To work around the issue, you can insert dummy column to the calculated column with empty string or insert to a staging table.

* Getting network connection error trying to fetch URL using Scala - **javax.net.ssl.SSLException: Connection reset**:
  
  1.Run this command in a notebook to create [init script](https://docs.microsoft.com/azure/databricks/clusters/init-scripts):
  
    ```
    dbutils.fs.put("dbfs:/databricks/ssl_change.sh","""
    #!/bin/bash
    echo "jdk.tls.disabledAlgorithms=anon, NULL" > /databricks/spark/dbconf/java/extra.security
    """,True)
    ```
    
  2.[Add init script path to cluster configuration](https://docs.microsoft.com/azure/databricks/clusters/init-scripts#--configure-a-cluster-scoped-init-script):
  
     ```
     dbfs:/databricks/ssl_change.sh
     ```
     
  3.Restart the cluster and test this scala code, it should run successfully:
     
     ```
     %scala val html = scala.io.Source.fromURL("https://azure.microsoft.com/api/v2/pricing/databricks/calculator/?currency=US").mkString’
     ```
## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [Running C++ Code in Scala](https://docs.microsoft.com/azure/databricks/kb/scala/running-c-plus-plus-code-scala)
* [How to Use Apache Spark Metrics](https://docs.microsoft.com/azure/databricks/kb/metrics/spark-metrics)
* [Drop Tables with Corrupted Metadata from the Metastore](https://docs.microsoft.com/azure/databricks/kb/metastore/drop-table-corruptedmetadata)
