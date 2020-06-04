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

Azure SQL Database Managed Instance enables you to load files from Azure Blob Storage. If you experience some issue while you are loading files from Azure Blob Storage, here you can find the actions that can help you to troubleshoot and mitigate the issue.

## **Recommended Steps**

Try some of the following steps to troubleshoot the issue:

- If you are noticing that some syntax error is returned by BULK INSERT or BULK INSERT check are you using supported syntax in this statement. As an example, if you are trying to load data via network share path note that this option is not supported in Azure SQL Database.
- Make sure that you are restoring a database from public blob storage protected with SAS credential. Private IPs for blob storage and service endpoints are currently not supported.
- If you are getting the error *5 (Access Denied)*, make sure that you have not denied the access to your Azure Blob Storage account using the firewall.
- Verify that you have created **EXTERNAL DATA SOURCE** with type **BLOB_STORAGE** targeting the URL of the blob storage where you placed the files that should be restored to your database.
- Make sure that you are targeting existing file on Azure blob storage.
- Script **EXTERNAL DATA SOURCE** and **CREDENTIAL** to SQL Server 2017 and try to load the files. If you are troubleshooting the issue on Managed Instance, make sure that SQL Server 2017 is in the subnet that is placed within the same VNet as the Managed Instance.
- Check is your SAS credential placed in **SECRET** option of **CREATE DATABASE SCOPED CREDENTIAL** statement valid. The most common errors in SAS token parameters are:
  - **?** is not removed from the beginning of the SAS token because the Azure portal generates SAS token with the leading ?. Remove this character if you see it.
  - **se** (expiry date) property is set to some value in the past (note that this is UTC time).
  - **st** (start date) property is not in the past (note that this is UTC time).
  - **sp** (permission) property should allow reading the file on the storage account.
  - **sip** (ip rage) remove this parameter if it is present in SAS token.

## **Recommended Documents**

- [Troubleshooting potential BULK INSERT/OPENROWSET issues on Azure SQL Database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-BULK-INSERT-and-OPENROWSET-issues-on-Azure-SQL/ba-p/664734)
