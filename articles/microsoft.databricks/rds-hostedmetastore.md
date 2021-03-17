<properties
	pageTitle="Diagnose and resolve issues with hosted metastore"
	description="Diagnose and resolve issues with hosted metastore"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677694"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1073b30d-bdb2-4702-a7f1-8a7a0f51cc30"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with hosted metastore

## **Recommended Steps**

* If Databricks cluster is experiencing **'METASTORE_DOWN'** frequently, interrupting processing and requiring a restart, it could be caused by a known issue of BoneCP not attempting to re-establish the broken connection after the issue happens. To workaround this behavior, you can use the new jar *hikari_datanucleus_2.11_0.1.jar* and copy it to */databricks/hive*:

	* Upload the jar *hikari-datanucleus.jar* to DBFS
	* Go to workspace, create Library, upload the file, and copy the path
	* Create init script using notebook:
 
    	```
    	%python
    
    	dbutils.fs.put("dbfs:/databricks/init_hikari/<clustername>/hikari.sh","""
    
    	#!/bin/bash
    	cp /dbfs/FileStore/jars/03390a65_418b_49d2_842e_a1069475b3d1-hikari_datanucleus_2_11_0_1-6bb4f.jar /databricks/hive
    	cp /databricks/jars/spark--maven-trees--spark_2.4--com.zaxxer--HikariCP--com.zaxxer__HikariCP__3.1.0.jar /databricks/hive
    
    	""",True)
    	```
    
	* Edit the cluster and add the below Spark configuration under Advanced Options:
    	```
    	spark.hadoop.datanucleus.connectionPoolingType hikari
    	```

	* Set up the init script in cluster, confirm changes, and launch the cluster

## **Recommended Documents**

* [Metastore Knowledge Base](https://docs.microsoft.com/azure/databricks/kb/metastore/)
* [How to Set Up Hive Metastore on SQL Server with Hive 2.0-2.2](https://docs.microsoft.com/azure/databricks/kb/metastore/set-up-sql-backed-hive-metastore)
* [How to Troubleshoot Several Apache Hive Metastore Problems](https://docs.microsoft.com/azure/databricks/kb/metastore/hive-metastore-troubleshooting)
