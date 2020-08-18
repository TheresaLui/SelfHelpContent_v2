<properties
	pageTitle="Cannot backup database of 1 TB or more to Page blob"
	description="Cannot backup database of 1 TB or more to Page blob"
	infoBubbleText="Cannot backup database of 1 TB or more to Page blob"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="d9d16cc5-e172-4de0-90d7-35bf3fb08743-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The error/symptom you see is because SQL Server limits the maximum backup size supported using a page blob to 1 TB.
<!--/issueDescription-->

## **Recommended Steps**
-  For SQL Server database backup to Microsoft Azure Blob storage account, there are two types of blobs that can be stored in the Microsoft Azure Blob storage service: block blobs and page blobs. Page blob has a limitation of 1 TB and block blobs can be used with SQL 2016 or later versions.
-  If you have SQL 2016 or later versions, then you can use block blob and backup your database using striped backups for up to 64 files(200 GB each file):
	```sql
	BACKUP DATABASE ... TO
		URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part01.bak',
		...
		URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part20.bak',
	WITH COMPRESSION, MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536, CHECKSUM, FORMAT, STATS = 5;
	```

- If you are on SQL 2O14 or below, then you need to backup this large database to locally, then compress file and copy to Azure Storage using AZ copy.

## **Recommended Documents**

* [Sql Server Backup To URL : Limitations](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?view=sql-server-ver15#limitations)
* [Backing up a VLDB to Azure Blob Storage](https://techcommunity.microsoft.com/t5/datacat/backing-up-a-vldb-to-azure-blob-storage/ba-p/305441#:~:text=To%20quote%20the%20relevant%20part,include%20up%20to%2050%2C000%20blocks.%E2%80%9D)
* [Copying SQL Server Backups to Windows Azure Storage using AzCopy](https://docs.microsoft.com/archive/blogs/dbrowne/copying-sql-server-backups-to-windows-azure-storage-using-azcopy)
* [Get started with AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10)