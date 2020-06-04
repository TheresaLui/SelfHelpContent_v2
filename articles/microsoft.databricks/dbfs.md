<properties
	pageTitle="Databricks DBFS"
	description="Databricks DBFS"
	service="microsoft.databricks"
	resource="workspaces"
	authors="mspreshah"
	ms.author="preshah"
	displayOrder="14"
	selfHelpType="resource"
	supportTopicIds="32612194"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8610f989-8e88-4c7e-a343-cccf5d1285ec"
	ownershipId="AzureData_AzureDatabricks"
/>

# Azure Databricks Databricks File System (DBFS)

## **Recommended Steps**

We recommend you create a [Azure Blob Store mount point](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-storage.html) or [Azure Data Lake Store Gen 1 mount point](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-datalake.html) on DBFS for Azure Blob Store to avoid having to provide credentials every time on access.    

Take the following into consideration when creating and configuring the Azure Databricks Databricks File System (DBFS):  

* You can access DBFS using the Databricks CLI, DBFS API, Databricks Utilities, Spark APIs or local file APIs
* Create a mount point only if you want ALL users in the Azure Databricks workspace to have access to the mounted storage
* Databricks Runtime 4.0 or higher is required to use this functionality
 
## **Recommended Documents**

* [Databricks File System](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html)  
* [Mount Azure Blob Storage containers with DBFS](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-storage.html)  
* [Mount Azure Data Lake Store with DBFS](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/azure-datalake.html)  

