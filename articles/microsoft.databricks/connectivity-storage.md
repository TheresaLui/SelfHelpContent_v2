<properties
	pageTitle="Diagnose and resolve conenctivity issues to storage resources"
	description="Diagnose and resolve conenctivity issues to storage resources"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677676"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="95b93b3e-58bf-4011-bbb0-4afa9a40e0b9"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues to storage resources

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

* [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2)

* [Access control in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control)

* [Tutorial: Access Azure Blob Storage from Azure Databricks using Azure Key Vault](https://docs.microsoft.com/azure/azure-databricks/store-secrets-azure-key-vault)

### **Configuration and Setup**

* Expiration of the secret key can cause issues connecting to storage resources. To recreate a secret, follow [these steps](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#create-a-new-application-secret)

* To read data from a private **Azure Blob Storage** account, you must configure a **Shared Key** or a **Shared Access Signature (SAS)**. Follow this [documentation](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-storage) for further details.

* If you are using a service principal and OAuth for authenticating storage, add AAD service endpoint to both subnets

### **Common Errors**

* [Network Configuration of Azure Data Lake Storage Gen1 Causes ADLException: Error getting info for file](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-gen1-issue)
* [Error When Reading Data from ADLS Gen 1 with Sparklyr](https://docs.microsoft.com/azure/databricks/kb/data-sources/access-adls1-from-sparklyr)
* Databricks is not able to access or mount ADLS anymore using a service principal and OAuth 2.0, resulting in **Bad Address** and **Error Enumerating Directory** error(s). This usually occurs when the application client secret is expired. To resolve the issue, you can create a new client secret and modify configs on the Databricks end accordingly.
	* [Create a new application secret](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#create-a-new-application-secret)
	* Access ADLS directly using a service principal and OAuth 2.0 - [ADLS Gen 1](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake#--access-directly-with-spark-apis-using-a-service-principal-and-oauth-20), [ADLS Gen 2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#--access-directly-with-service-principal-and-oauth-20)
	* Mount ADLS using a service principal and OAuth 2.0 - [ADLS Gen 1](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake#--mount-azure-data-lake-storage-gen1-resource-using-a-service-principal-and-oauth-20), [ADLS Gen 2](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2#--mount-an-azure-data-lake-storage-gen2-account-using-a-service-principal-and-oauth-20)
