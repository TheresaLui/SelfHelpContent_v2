<properties
	pageTitle="Databricks DBFS"
	description="Databricks DBFS"
	service="microsoft.databricks"
	resource="clusters"
	authors="mspreshah"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32612194"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
/>

# Azure Databricks Databricks File System (DBFS)

## **Recommended steps**

We recommend you create a [Azure Blob Store mount point](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-storage.html) or [Azure Data Lake Store Gen 1 mount point](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-datalake.html) on DBFS for Azure Blob Store to avoid having to provide credentials every time on access.    

Take the following into consideration when creating and configuring the Azure Databricks Databricks File System (DBFS):  

* ADLS Gen 2 mount points are not supported as of yet 
* You can access DBFS using the Databricks CLI, DBFS API, Databricks Utilities, Spark APIs or local file APIs.  
* Create a mount point only if you want ALL users in the Azure Databricks workspace to have access to the mounted storage.  
* Databricks Runtime 4.0 or higher is required to use this functionality.  
 
## **Recommended documents**
* [Databricks File System](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html)  
* [Mount Azure Blob Storage containers with DBFS](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-storage.html)  
* [Mount Azure Data Lake Store with DBFS](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-datalake.html)  

