<properties
  pagetitle="Database Backup or Restore Using Disk"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740095"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="9f6a2886-f594-4ae7-832f-706841ee5a8e"
  ownershipid="AzureData_AzureSQLVM" />
# Database Backup or Restore Using Disk

Most of the users are able to resolve their SQL Server Database Backup to Disk issues by following below articles:


## Common Issues

 * **Error 3035: Cannot perform a differential backup for database "dbName", because a current database backup does not exist.**

   This can occur if you have configured [Azure Backup service](https://docs.microsoft.com/azure/backup/backup-overview) to backup SQL databases or VM Snapshot which does not do a copy only backup causing your Maintenance plan or SQL Agent job , Ad hoc backups to fail

   To fix this, [Add the following registry keys](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues) on each of the VMs hosting SQL server instances and where VM backups are configured and post this change backups will not fail:
    ```PS
    [HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\BCDRAGENT]  
    "USEVSSCOPYBACKUP"="TRUE" 
    ```
* **Migrate Databases or Export Data from On Premise/Another Cloud to Azure VM**

  If you have a planned downtime to migrate your databases, then you can use the following options: 

  [Backup ](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?redirectedfrom=MSDN&view=sql-server-ver15#complete)and [Restore](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=sql-server-ver15#Azure_Blob) using URL feature, [AzCopy tool](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/), [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/), [Backup to Microsoft Azure Tool](https://blogs.technet.microsoft.com/dataplatforminsider/2014/07/24/get-started-backing-up-to-the-cloud-with-sql-server-backup-to-microsoft-azure-tool/) for SQL 2008/R2 version, [Azure Backup and Site Recovery
](https://docs.microsoft.com/azure/backup/)

  If you do not have a downtime and want to migrate your databases, then only option to go with is [Setting up a hybrid Always on](https://docs.microsoft.com/previous-versions/azure/virtual-machines/windows/sqlclassic/virtual-machines-windows-classic-sql-onprem-availability#add-azure-replica-wizard)  group between your on prem and Azure and fail that over to Azure.  
  
  If you want to export schema, you can use [DACPAC](https://docs.microsoft.com/sql/relational-databases/data-tier-applications/extract-a-dac-from-a-database?view=sql-server-ver15)

* **Backup database with AG**

  When the backup preference is set to [Prefer secondary in the AG](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-backup-on-availability-replicas-sql-server?view=sql-server-ver15), the user database backup will not be generated on the primary replica when a backup is configured using the Backup Database Task in a Maintenance Plan.  This is because the Backup Database Task in a Maintenance Plan automatically adds a check to determine if the current replica is the preferred backup replica for databases in the AG.  If the replica is the preferred replica for backup, then the BACKUP DATABASE command will execute, otherwise the database backup will be skipped. 




## **Recommended Documents**

* [Troubleshooting SQL Server backup and restore operations](https://support.microsoft.com/help/224071/troubleshooting-sql-server-backup-and-restore-operations)
* [SQL Server DBA: Backup error and solutions](https://social.technet.microsoft.com/wiki/contents/articles/51188.sql-server-dba-backup-error-and-solutions.aspx)
* [Possible Media Errors During Backup and Restore](https://docs.microsoft.com/sql/relational-databases/backup-restore/possible-media-errors-during-backup-and-restore-sql-server?view=sql-server-ver15)
* [SQL Server Backup Overview](https://docs.microsoft.com/sql/relational-databases/backup-restore/backup-overview-sql-server?view=sql-server-ver15)
* [SQL Server System Databases Backup & Restore](https://docs.microsoft.com/sql/relational-databases/backup-restore/back-up-and-restore-of-system-databases-sql-server?view=sql-server-ver15)
* [SQL Server Backup History and Header Information](https://docs.microsoft.com/sql/relational-databases/backup-restore/backup-history-and-header-information-sql-server?view=sql-server-ver15)