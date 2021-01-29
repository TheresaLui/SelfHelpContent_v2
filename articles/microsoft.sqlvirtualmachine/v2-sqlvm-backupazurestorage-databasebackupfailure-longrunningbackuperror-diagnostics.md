<properties
	pageTitle="Long Running Backup"
	description="Long Running Backup"
    infoBubbleText="Long Running Backup"
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
	articleId="a5569687-455e-467d-9647-f6761f96fbf6-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The issue can be due to multiple reasons. Make sure you have followed the recommended steps listed below.

<!--/issueDescription-->
## **Recommended Steps**

For slow Backups, please verify the following:
- You are using compression option in backup parameters.
- Striping the backups can help in speeding up the backup process. Please make sure to use MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536 in the backup parameters. Example below:
	```sql
	BACKUP DATABASE ... TO
		URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part01.bak',
		...
		URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part20.bak',
	WITH COMPRESSION, MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536, CHECKSUM, FORMAT, STATS = 5;
	```

- Make sure you have antivirus exceptions in place as listed at:
		https://support.microsoft.com/help/309422/choosing-antivirus-software-for-computers-that-run-sql-server

For slow Restore, please verify the following:
- You have added SQL Service Account to Perform Volume Maintenance Tasks in secpol.msc
- Check for antivirus exceptions and filter drivers.
- Increase the buffer count to restore faster for large databases
- Many slow restore cases were fixed by adding trace flag 3235. We need to add this as the disk bytes per physical sector on Azure is 4k.
- Make sure you are already following SQL VM Performance best practices guidelines: https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices


## **Recommended Documents**

* [Performance guidelines for SQL Server on Azure Virtual Machines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices)


