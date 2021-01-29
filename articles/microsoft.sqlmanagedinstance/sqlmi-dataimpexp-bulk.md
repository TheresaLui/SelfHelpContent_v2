<properties
	pageTitle="Management/Loading data from Azure Blob Storage"
	description="Management/Loading data from Azure Blob Storage"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637242"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="1e3d1a25-46c9-4f7b-8298-804e38f4fe2a"
	ownershipId="AzureData_AzureSQLMI"
/>

# Troubleshoot loading from Azure blob storage

Azure SQL Database Managed Instance enables you to load files from Azure Blob Storage using [OPENROWSET function](https://docs.microsoft.com/sql/t-sql/functions/openrowset-transact-sql?view=sql-server-ver15#using-openrowset-with-the-bulk-option) or [BULK INSERT](https://docs.microsoft.com/sql/t-sql/statements/bulk-insert-transact-sql?view=sql-server-ver15). Most users can resolve issues while loading files from Azure Blob Storage by using the following steps. 

## **Recommended Steps**

- If a syntax error is returned by BULK INSERT or BULK INSERT, check if you're using supported syntax in the statement. For example, if you're trying to load data via the network share path, this option is not supported in Azure SQL Database.
- Make sure that you are restoring a database from public blob storage protected with SAS credentials. Private IPs for blob storage and service endpoints are currently not supported.
- If you are getting the error 5 (Access Denied), **make sure that you have not denied the access to your Azure Blob Storage account using the firewall**.
- Verify that you have created **EXTERNAL DATA SOURCE** with type **BLOB_STORAGE** targeting the URL of the blob storage where you placed the files that should be restored to your database.
- Make sure that you are targeting existing files on Azure blob storage. Azure Data Lake is not supported.
- Make sure that you are loading data using valid [Shared Access Signature (SAS token)](https://docs.microsoft.com/sql/t-sql/statements/bulk-insert-transact-sql?view=sql-server-ver15#f-importing-data-from-a-file-in-azure-blob-storage). Azure Active Directory authentication or [Managed identity of Azure SQL service](https://docs.microsoft.com/azure/azure-sql/database/doc-changes-updates-release-notes?tabs=single-database#bulk-insert-and-backuprestore-statements-cannot-use-managed-identity-to-access-azure-storage) are currently not supported.
- Script **EXTERNAL DATA SOURCE** and **CREDENTIAL** to SQL Server 2017 and try to load the files. If you are troubleshooting the issue on Managed Instance, make sure that SQL Server 2017 is in the subnet that is placed within the same VNet as the Managed Instance.
- Check if your SAS credential placed in **SECRET** option of **CREATE DATABASE SCOPED CREDENTIAL** statement is valid. The most common errors in SAS token parameters are:
  - **?** is not removed from the beginning of the SAS token because the Azure portal generates SAS token with the leading ?. Remove this character if you see it.
  - **se** (expiry date) property is set to some value in the past (note that this is UTC time).
  - **st** (start date) property is not in the past (note that this is UTC time).
  - **sp** (permission) property should allow reading the file on the storage account.
  - **sip** (ip rage) remove this parameter if it is present in SAS token.

## **Recommended Documents**

- [Loading data using Shared Access Signature](https://docs.microsoft.com/sql/t-sql/statements/bulk-insert-transact-sql?view=sql-server-ver15#f-importing-data-from-a-file-in-azure-blob-storage)
- [Troubleshooting potential BULK INSERT/OPENROWSET issues on Azure SQL Database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-BULK-INSERT-and-OPENROWSET-issues-on-Azure-SQL/ba-p/664734)
