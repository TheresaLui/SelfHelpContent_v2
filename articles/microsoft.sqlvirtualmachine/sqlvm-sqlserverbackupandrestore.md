<properties
	pageTitle="backup/sql server backup and restore"
	description="backup/sql server backup and restore"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32633516"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	articleId="bc8b4aab-73b3-415d-9222-61a3e5d69386"
	ownershipId="AzureData_AzureSQLVM"
/>

# backup/sql server backup and restore

* **Differential backups are failing when VM backup is enabled**

	By default, Azure VM backup creates a [VSS full backup](https://techcommunity.microsoft.com/t5/Storage-at-Microsoft/What-is-the-difference-between-VSS-Full-Backup-and-VSS-Copy/ba-p/423575) on Windows VM which can break the backup chain for differentials. So, when it does a VSS full backup, it creates backup of all the files – but after that, the backup application may truncate logs on the file system. This breaks the backup chain for differentials. 

	On the other hand, when you do a VSS copy backup, all files are backed up and you preserve all the applications files including log files on the live system. 

	You can enable VSS copy backup through registry key.  
	`REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgent" /v USEVSSCOPYBACKUP /t REG_SZ /d TRUE /f `

	Once the key is in place, take a full backup of SQL Server and differential backup will start working correctly. 

* **Backup is not running**

	Ensure SQL Server Agent service is Started and Running. SQL Server Managed Backup to Microsoft Azure requires SQL Server Agent to be running on the instance to perform backup operations. 

	You may want to set SQL Server Agent to run automatically on Windows startup. You can also ensure <a href="https://docs.microsoft.com/previous-versions/technet-magazine/gg313742(v=msdn.10)">SQL Server Agent is set to restart SQL services automatically</a> in case they stop unexpectedly.  

* **Backup status alerts**

	You can enable email notifications to receive backup errors and warnings. See [Enable and Configure Notification for Health Status](https://docs.microsoft.com/sql/relational-databases/backup-restore/enable-sql-server-managed-backup-to-microsoft-azure?view=sql-server-2017&tabs=azure-cli#enable-managed-backup-to-azure).

* **Backup for databases larger than 1 TB**

	Backup to URL with page blob allows backup sizes up to 1 TB. Starting with SQL Server 2016, backup to URL supports block blob allowing backup sizes up to 12 TB. Consider striping, COMPRESSION, MAXTRANSFERSIZE and BLOCKSIZE when backing up large databases to block blob. See [Backing up a VLDB to Azure Blob Storage](https://blogs.msdn.microsoft.com/sqlcat/2017/03/10/backing-up-a-vldb-to-azure-blob-storage/). 
 
	For backup sizes beyond 12 TB, consider [backup to local disk and use azcopy](https://blogs.msdn.microsoft.com/dbrowne/2014/03/07/copying-sql-server-backups-to-windows-azure-storage-using-azcopy/) to upload to storage. 

* **Backup to URL (page blob) intermittently fails**

	> Error message: Backup to URL received an exception from the remote endpoint. Exception Message: The client could not finish the operation within specified timeout. 

	When you back up your databases to Azure Page Blobs by using BackuptoURL statements, SQL server internally calls a stand-alone application named BackuptoURL.exe. This problem occurs because the BackuptoURL application does not correctly handle transient failures. This issue has been fixed in a cumulative update.

	Ensure you have the latest patches applied for SQL server. Details about the issue are listed [here](https://support.microsoft.com/help/4463320/sql-server-backups-to-azure-blob-storage-intermittent-failure). 


## **Recommended Documents**

* [Automated Backup for Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-backup-v2)<br>
* [SQL Server Backup to URL Best Practices and Troubleshooting](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url-best-practices-and-troubleshooting?view=sql-server-2017)<br>
* [File-Snapshot Backups for Database Files in Azure](https://docs.microsoft.com/sql/relational-databases/backup-restore/file-snapshot-backups-for-database-files-in-azure?view=sql-server-2017)<br>
* [SQL Server Managed Backup to Microsoft Azure](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-managed-backup-to-microsoft-azure?view=sql-server-2017)
