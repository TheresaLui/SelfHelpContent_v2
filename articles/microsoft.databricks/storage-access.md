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

## **Common Errors**

* Databricks is not able to access/mount ADLS anymore using a service principal and OAuth 2.0 getting **Bad Address** and **Error Enumerating Directory** error(s). This usually occurs when application client secret is expired. To resolve the issue, you can create a new client secret and modify configs on Databricks end accordingly.
	* [Create a new application secret](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#create-a-new-application-secret)
	* Access ADLS directly using a service principal and OAuth 2.0 - [ADLS Gen 1](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake#--access-directly-with-spark-apis-using-a-service-principal-and-oauth-20), [ADLS Gen 2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#--access-directly-with-service-principal-and-oauth-20)
	* Mount ADLS using a service principal and OAuth 2.0 - [ADLS Gen 1](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake#--mount-azure-data-lake-storage-gen1-resource-using-a-service-principal-and-oauth-20), [ADLS Gen 2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#--mount-an-azure-data-lake-storage-gen2-account-using-a-service-principal-and-oauth-20)

## **Recommended Documents**

* [Cannot Read Azure Databricks Objects Stored in DBFS Root Directory](https://kb.azuredatabricks.net/dbfs/dbfs-root-permissions.html)
