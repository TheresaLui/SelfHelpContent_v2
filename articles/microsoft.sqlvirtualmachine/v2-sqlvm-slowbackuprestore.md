<properties
  pagetitle="SQL Database Backup or Restore is Slow"
  service="microsoft.compute"
  resource="virtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32748893"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="734cb41c-d6e8-449e-9a6b-b7512b4c9684"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Database Backup or Restore is Slow

Most users are able to resolve their issues with SQL Server Replication using the recommended documents below.

## **Recommended Steps**

* **For Slow Backups, please verify the following:**

	- You are using **compression** option in backup parameters
	- For SQL 2014 or below, try to tweak the [**Buffer Count**](https://docs.microsoft.com/sql/t-sql/statements/backup-transact-sql?view=sql-server-ver15#with-options) parameter to speed up backups
	- Make sure you have [Antivirus Exceptions](https://support.microsoft.com/help/309422/choosing-antivirus-software-for-computers-that-run-sql-server) in place 
      
* **If you are having a slow performance backing the database to URL:**

	- Please follow the above basic checks
	- Check if the VM or disk is getting throttled affecting the backup process. Quick way to workaround is to resize the VM/Disk.
	- Striping the backups can help in speeding up the backup process. Please make sure to use **MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536** in the backup parameters if you are using SQL 2016 or above. Example below: 
      
      ```SQL
      BACKUP DATABASE … TO 
      URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part01.bak', 
      … 
      URL = 'https://storageaccount.blob.core.windows.net/backup/DB_part20.bak', 
      WITH COMPRESSION, MAXTRANSFERSIZE = 4194304, BLOCKSIZE = 65536, CHECKSUM, FORMAT, STATS = 5; 
      ```

* **For Slow Restore, please verify the following:**

  - You have added SQL Service Account to [Perform Volume Maintenance Tasks](https://docs.microsoft.com/sql/relational-databases/databases/database-instant-file-initialization?view=sql-server-ver15) in secpol.msc 
  - Check for [Antivirus exceptions](https://support.microsoft.com/help/309422/choosing-antivirus-software-for-computers-that-run-sql-server) and [filter drivers](https://support.microsoft.com/help/2454053/use-of-system-filter-drivers-can-lead-to-sql-server-database-engine-pe). Disable antivirus and try restore.
  - Increase the [Buffer Count](https://docs.microsoft.com/sql/t-sql/statements/backup-transact-sql?view=sql-server-ver15#with-options) to restore faster for large databases
  - Recovery of database for restore can be slow if you have [Large log file for the database with active VLFs](https://support.microsoft.com/help/2455009/fix-slow-performance-when-you-recover-a-database-if-there-are-many-vlf)
      
* **If you are having a slow performance restoring the database from URL:**
   
	- Please follow the above basic checks
	- Many slow restore cases were fixed by following the article [Slow Restore on disk with 4K Sector size](https://support.microsoft.com/help/4088193/slow-performance-on-restoring-compressed-backup-on-disk-with-4k-sector)
	- Check if the VM or disk is throttled affecting the restore performance. Quick way to work around is to resize the VM/Disk to the next size.

## **Recommended Documents**

* [Troubleshoot Slow backup and Restore](https://support.microsoft.com/help/224071/troubleshooting-sql-server-backup-and-restore-operations)
* [Optimize Backup and Restore Performance](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms190954%28v=sql.105%29?redirectedfrom=MSDN)
