<properties
	pageTitle="Delta table query performance is slow when underlying data directory is in ADLS Gen2 file system"
	description="Delta table query performance is slow when underlying data directory is in ADLS Gen2 file system"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6e1d1a62-520c-4021-a5cf-cd836fed905b"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Delta table query performance is slow when underlying data directory is in ADLS Gen2 file system

**Problem**

Query against delta table is slow when the delta table’s data is in ADLS Gen2 filesystem
This problem affects clusters on Databricks Runtime 5.4 or earlier.

**Troubleshooting**

* Verify if they are using DBR 5.4 or earlier version
* Verify if the storage system being used is ADLS Gen2

**Cause**

The DBR 5.4 and earlier versions check for the latest version of a Delta Lake table on ADLS Gen2 by listing all available versions and then finds the latest version of Delta table.

**Solution**

In DBR 5.5, improvement has been made to check only the end of the transaction log instead of listing all available versions. This optimization makes update a constant time operation, and significantly improving the latency. Use DBR 5.5 or above to see improvement in the Delta table query performance.
