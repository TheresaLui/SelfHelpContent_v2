<properties
  pagetitle="Database Backup or Restore using URL (Azure Storage)"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740094"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="37aa2d07-83df-4ce9-9810-a098f1065cbd-azurestorage"
  ownershipid="AzureData_AzureSQLVM" />
# Database Backup or Restore using URL (Azure Storage)

## Common Issues


 Most users are able to resolve their issues with SQL Server database backup to Azure storage (Backup to URL) using the recommended documents below.

* **Error 3063: Backup to URL With SAS fails with the error:"Device has reached its limit of allowed blocks" or "The request could not be performed because of an I/O device error"**

  To fix this issue, [Stripe your backup](https://docs.microsoft.com/archive/blogs/sqlcat/backing-up-a-vldb-to-azure-blob-storage) target with multiple files with below parameters: 
  
   ```SQL
    BACKUP DATABASE … TO 
    URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part01.bak', 
    … 
    URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part20.bak', 
    WITH COMPRESSION, MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536,CHECKSUM, FORMAT, STATS = 5;
    ```

* **Migrate Databases or Export Data from On Premise/Another Cloud to Azure VM**

 If you have a planned downtime to migrate your databases, then you can use the following options: 
 
  * [Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?redirectedfrom=MSDN&view=sql-server-ver15#complete)
  * [Restore](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=sql-server-ver15#Azure_Blob) using URL feature
  * [AzCopy tool](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/)
  * [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/)
  * [Backup to Microsoft Azure Tool](https://blogs.technet.microsoft.com/dataplatforminsider/2014/07/24/get-started-backing-up-to-the-cloud-with-sql-server-backup-to-microsoft-azure-tool/) for SQL 2008/R2 version
  * [Azure Backup and Site Recovery](https://docs.microsoft.com/azure/backup/)
  
  If you do not have a downtime and want to migrate your databases, then only option to go with is [Setting up a hybrid Always on](https://docs.microsoft.com/previous-versions/azure/virtual-machines/windows/sqlclassic/virtual-machines-windows-classic-sql-onprem-availability#add-azure-replica-wizard) group between your on prem and Azure and fail that over to Azure.  

* **Error 3271: Backup fails due to TLS or .Net with the error "Backup to URL received an exception from the remote endpoint"**

  This can happen on SQL 2012,2014 and 2016. Backup to Microsoft Azure blob storage service URL isn’t compatible for TLS 1.2 and can be fixed by following this [KB article](https://support.microsoft.com/help/4017023/fix-sql-server-2014-or-2016-backup-to-microsoft-azure-blob-storage-ser).

* **Error 45207: A container URL was either not provided or invalid**

   To fix this issue, please navigate to Azure Portal --> Storage Account --> Configuration --> "Allow Blob Public Access"

* **Error 416: Cannot backup database of more than 1 TB on SQL 2014 or lower versions due to "The remote server returned an error: (416) The page range specified is invalid"**

  SQL Server supports up to 1 TB when using backup to URL using Page blobs. Try using compression in the backup command parameters to see if database backup file size can be lowered than 1 TB. If that does not work for you, we recommend to [Backup to disk](https://docs.microsoft.com/sql/t-sql/statements/backup-transact-sql?view=sql-server-ver15), [Azure Backup service](https://docs.microsoft.com/azure/backup/backup-overview) or [Upgrade your SQL to 2016 or later](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version) and [Use backup to URL with SAS](https://blogs.msdn.microsoft.com/sqlcat/2017/03/10/backing-up-a-vldb-to-azure-blob-storage/) so that backup can use block blobs.

* **Error 3201: Cannot backup database to URL fails with the error "Operating system error 50(The request is not supported.)"**

  Verify if the SAS token is not more than 128 characters. Remove the question mark symbol (?) from the SAS token. Please make sure you can connect to the storage account from the current machine using Storage explorer or SSMS and port 443 is open for outbound connections. 
  
  Make sure the policy assigned to SAS token is not expired. You can [Create a new Policy](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-storage-explorer#manage-access-policies) using Azure storage explorer and create a new SAS token  with that policy from Azure storage explorer. [Re-create the credential](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?view=sql-server-ver15#credential) using this new token and try backing up again.

* **Error 3035: Cannot perform a differential backup for database "DBname", because a current database backup does not exist.**

  This can occur if you have configured [Azure Backup service](https://docs.microsoft.com/azure/backup/backup-overview) to backup SQL databases or VM Snapshot which does not do a copy only backup causing your Maintenance plan or SQL Agent job , Ad hoc backups to fail. 
  
  To fix this, [Add the following registry keys](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues) on each of the VMs hosting SQL server instances and where VM backups are configured and post this change backups will not fail:
  
  ```PS
  [HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\BCDRAGENT]  
  "USEVSSCOPYBACKUP"="TRUE" 
  ```

## **Recommended Documents**

* [SQL Server Backup to URL Common Errors and Troubleshooting](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url-best-practices-and-troubleshooting?view=sql-server-ver15)
* [Setup or Configure SQL Server Backup to URL](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url?view=sql-server-ver15)
* [SQL Server Backup to URL – a cheat sheet](https://techcommunity.microsoft.com/t5/datacat/sql-server-backup-to-url-a-cheat-sheet/ba-p/346358)
* [SQL Server Backup and Restore with Microsoft Azure Blob Storage Service](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-and-restore-with-microsoft-azure-blob-storage-service?view=sql-server-ver15)
* [Tutorial: Use Azure Blob storage service with SQL Server 2016](https://docs.microsoft.com/sql/relational-databases/tutorial-use-azure-blob-storage-service-with-sql-server-2016?view=sql-server-ver15)
* [Use Azure Storage for SQL Server Backup and Restore](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-use-storage-sql-server-backup-restore)
* [Restoring From Backups Stored in Microsoft Azure](https://docs.microsoft.com/sql/relational-databases/backup-restore/restoring-from-backups-stored-in-microsoft-azure?view=sql-server-ver15)
