<properties
	pageTitle="Databricks DBFS"
	description="Databricks DBFS"
	service="microsoft.databricks"
	resource="clusters"
	authors="mspreshah"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32612194"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
/>

# Azure Databricks Databricks File System (DBFS)

## **Recommended steps**

The folllowing details refer to the Databricks File System (DBFS)

(1) Create a mount point on DBFS for Azure Blob Store or Azure Data Lake Store Gen 1 to avoid having to provide credentials every time on access.  
(2) Create a mount point only if you want ALL users in the Azure Databricks workspace to have access to the mounted storage.  
(3) Databricks Runtime 4.0 or higher is required to use this functionality.  
(4) Access DBFS using the Databricks CLI, DBFS API, Databricks Utilities, Spark APIs or local file APIs.  
(5) Note: ADLS Gen 2 mount points are not supported as of yet  

## **Recommended documents**
1. [Databricks File System](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html)  
2. [Mount Azure Blob Storage containers with DBFS](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-storage.html)  
3. [Mount Azure Data Lake Store with DBFS](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-datalake.html)  

