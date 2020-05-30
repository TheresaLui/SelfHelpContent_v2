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

Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

### **Configuration and Setup**

* [Access control in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control)
* Expiration of secret key can cause issues connecting to storage resources. To recreate secret please follow [these steps](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#create-a-new-application-secret)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip#how-to-assign-a-single-public-ip-for-vnet-injected-workspaces-using-azure-firewall)
* [Azure Data Lake Storage Gen2](https://docs.databricks.com/data/data-sources/azure/azure-datalake-gen2.html)
* [FAQ-Azure Data Lake Storage Gen2](https://docs.databricks.com/data/data-sources/azure/azure-datalake-gen2.html#frequently-asked-questions-faq)
* [Azure Data Lake Storage Gen1](https://docs.databricks.com/data/data-sources/azure/azure-datalake.html)
* [Tutorial: Access Azure Blob Storage from Azure Databricks using Azure Key Vault](https://docs.microsoft.com/azure/azure-databricks/store-secrets-azure-key-vault)
* If you are using Service principal and oauth for authenticating storage, please add AAD service endpoint to both subnets

### **Common Errors**

* [Network Configuration of Azure Data Lake Storage Gen1 Causes ADLException: Error getting info for file](https://kb.azuredatabricks.net/cloud/azure-vnet-gen1-issue.html#problem-network-configuration-of-azure-data-lake-storage-gen1-causes-adlexception-error-getting-info-for-file)
* [Error When Reading Data from ADLS Gen 1 with Sparklyr](https://kb.azuredatabricks.net/data-sources/access-adls1-from-sparklyr.html#problem-error-when-reading-data-from-adls-gen-1-with-sparklyr)
