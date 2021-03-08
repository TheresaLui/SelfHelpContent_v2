<properties
	pageTitle="Resolve bulk insert related errors and exceptions"
	description="Resolve bulk insert related errors and exceptions"
	infoBubbleText="Resolve bulk insert related errors and exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="1"
	selfHelpType="diagnostics"
	supportTopicIds="32749519"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
	resourceTags="servers, databases"
	articleId="9c48a09f-8a15-46ad-b658-20a0d970524f"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve bulk insert related errors and exceptions

<!--issueDescription-->
These are the most commonly used steps to resolve bulk insert issues.
<!--/issueDescription-->


### Performance considerations

If the number of pages to be flushed in a single batch exceeds an internal threshold, a full scan of the buffer pool might occur to identify which pages to flush when the batch commits. This full scan can hurt bulk-import performance. A likely case of exceeding the internal threshold occurs when a large buffer pool is combined with a slow I/O subsystem. To avoid buffer overflows on large machines, either do not use the TABLOCK hint (which will remove the bulk optimizations) or use a smaller batch size (which preserves the bulk optimizations).

We recommend that you test various batch sizes with your data load to find out what works best for you.
With Azure SQL Database, consider temporarily increasing the performance level of the database or instance prior to the import if you are importing a large volume of data.

### Common configuration and syntax issues

Azure SQL Database (single database and Managed Instance) enables you to [load files from Azure Blob Storage](https://techcommunity.microsoft.com/t5/azure-sql/loading-files-from-azure-blob-storage-into-azure-sql-database/ba-p/386133)

* If you are noticing that a syntax error is returned by BULK INSERT or BULK INSERT check that you are using [supported syntax](https://docs.microsoft.com/azure/azure-sql/managed-instance/transact-sql-tsql-differences-sql-server#bulk-insert--openrowset) in this statement. As an example, if you are trying to load data via network share path note that this option is not supported in Managed Instance.
* Make sure that you are using SAS key to access storage. Azure AD identities and managed identities are currently [not supported](https://docs.microsoft.com/azure/azure-sql/database/doc-changes-updates-release-notes?tabs=single-database#bulk-insert-and-backuprestore-statements-cannot-use-managed-identity-to-access-azure-storage).
* Make sure that you are reading data from a public blob storage protected with [SAS credential](https://docs.microsoft.com/azure/storage/common/storage-sas-overview?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json). Private IPs for blob storage and service endpoints are currently not supported.
* If you are getting an error 5 (Access Denied), make sure that you have not denied access to your Azure Blob Storage account using the firewall.
*Verify that you have created the EXTERNAL DATA SOURCE with type BLOB_STORAGE targeting the URL of the blob storage where you placed the files that should be restored to your database.
* Make sure that you are targeting an existing file on Azure blob storage.
* Script the CREDENTIAL to SQL Server 2017 and try to load the files. If you are troubleshooting the issue on Managed Instance make sure that SQL Server is in the subnet that is within the same VNet as the Managed Instance.
* Check if your SAS credential placed in the SECRET option of the CREATE DATABASE SCOPED CREDENTIAL statement valid. The most common errors in SAS token parameters are:
? is not removed from the beginning of the SAS token because the Azure portal generates SAS token with the leading ?. Remove this character if you see it.
se (expiry date) property is set to some value in the past (note that this is UTC time).
st (start date) property is not in the past (note that this is UTC time).
sp (permission) property should allow reading the file on the storage account.
sip (ip range) remove this parameter if it is present in SAS token.

## **Recommended Documents**

[BULK INSERT](https://docs.microsoft.com/sql/t-sql/statements/bulk-insert-transact-sql?view=sql-server-ver15)


