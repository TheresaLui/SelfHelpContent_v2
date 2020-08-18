<properties
	pageTitle="Database Backup Failure with blob limit"
	description="Backup to Storage Account with SAS Fails with Error: Device has reached its limit of allowed blocks"
	infoBubbleText="Database Backup Failure with blob limit"
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
	articleId="42eadd64-e7f2-4c42-a474-1e6b847c55b3-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The error returned indicates you are hitting the 50k block blob limit as your database size is large.
<!--/issueDescription-->

## **Recommended Steps**

- Since Azure blob block has 50K limit, if your database is very big you may hit the 50K limitation. For example, your backup command may fail with "Device has reached its limit of allowed blocks".
-  Max size of block blob = 195 GB. Each block blob comprises of multiple smaller blocks - up to 50,000. Each of these blocks can be of varying size - (max of 4 MB for SQL server - limitation of REST API used by SQL). SQL by default writes 1 MB blocks - so when the individual backup file is more than 48GB (50,000 x 1 MB) - you get this error. We recommend you use MAXTRANSFERSIZE = 
 4194304, BLOCKSIZE = 65536 and COMPRESSION to avoid the limitation causing this failure
- One best practice is to stripe your backup target with multiple files, for example, you can backup to max 64 files this way:
	```sql
	BACKUP DATABASE ... TO
		URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part01.bak',
		...
		URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part20.bak',
	WITH COMPRESSION, MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536, CHECKSUM, FORMAT, STATS = 5;
	```

## **Recommended Documents**

* [Backing up a VLDB to Azure Blob Storage](https://techcommunity.microsoft.com/t5/datacat/backing-up-a-vldb-to-azure-blob-storage/ba-p/305441#:~:text=To%20quote%20the%20relevant%20part,include%20up%20to%2050%2C000%20blocks.%E2%80%9D)



