<properties
	pageTitle="Diagnose and resolve issues with Storage access"
	description="Diagnose and resolve issues with Storage access"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677689"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3c9fd427-f683-4cff-bda1-96c1b5eacfa6"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Storage access

## **Recommended Steps**

* Review [How To: Four ways of accessing Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#---access-automatically-with-your-azure-active-directory-credentials)

* When using Azure Databricks, it can be confusing when a new workspace and managed resource group appear. Azure automatically creates a **Databricks workspace**, as well as a **managed resource group (databricks-rg-xxx-xxx)** that contains all the resources needed to run the cluster. 

  This managed resource group (MRG) is protected by a system-level lock to prevent deletions and modifications. The only way to directly remove the lock is to delete the service. However, by making changes to the parent resource group, those changes will be correspondingly updated in the managed resource group.

* [Resolve issue: When I accessed an Azure Data Lake Storage Gen2 account with the hierarchical namespace enabled, I experienced a java.io.FileNotFoundException error, and the error message includes FilesystemNotFound](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#frequently-asked-questions-faq)

* [Resolve issue: I observe the error "This request is not authorized to perform this operation using this permission" when I try to mount an Azure Data Lake Storage Gen2 filesystem](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#frequently-asked-questions-faq)

* Issue: If Databricks is not able to access/mount ADLS using a service principal and OAuth 2.0 is getting **Bad Address** and **Error Enumerating Directory** error(s), this is usually because the application client secret is expired. To resolve the issue, create a new client secret and modify configs on Databricks end accordingly:
	* [Create a new application secret](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#create-a-new-application-secret)
	* Access ADLS directly using a service principal and OAuth 2.0 - [ADLS Gen 1](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake#--access-directly-with-spark-apis-using-a-service-principal-and-oauth-20), [ADLS Gen 2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#--access-directly-with-service-principal-and-oauth-20)
	* Mount ADLS using a service principal and OAuth 2.0 - [ADLS Gen 1](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake#--mount-azure-data-lake-storage-gen1-resource-using-a-service-principal-and-oauth-20), [ADLS Gen 2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#--mount-an-azure-data-lake-storage-gen2-account-using-a-service-principal-and-oauth-20)
	
* Not able to connect to Azure SQL DW using managed identity and ADLS from Databricks, getting an error similar to:

    ```
    com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
    com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]
    ```
  This issue is most likely due to managed identity misconfiguration on Azure SQL DW. To resolve it, follow [steps 1 and 3 in this document](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).

* [Avoiding error 403 (request not authorized) when accessing ADLS Gen 2 from Azure Databricks while using a Service Principal](https://deep.data.blog/2019/03/28/avoiding-error-403-request-not-authorized-when-accessing-adls-gen-2-from-azure-databricks-while-using-a-service-principal/)

## **Recommended Documents**

* [Cannot Read Azure Databricks Objects Stored in DBFS Root Directory](https://docs.microsoft.com/azure/databricks/kb/dbfs/dbfs-root-permissions)
