<properties
  pagetitle="Database Space Issues &#xD;"
  description="Database Space Issues"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740079"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="f31fbaea-cfc8-407e-9be1-4dfe4bd4f410"
  ownershipid="AzureData_AzureSQLVM" />
# Database Space Issues 

Most users can resolve their issues with Database Space by using the following steps. 

## **Recommended Steps** 

* **Transaction Log taking the disk space** 

   * If your log is full, check if your [log file growth is set to unrestricted](https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file?view=sql-server-ver15) 

   * There are many [**factors that don't allow truncating the log file**](https://docs.microsoft.com/sql/relational-databases/logs/the-transaction-log-sql-server?view=sql-server-ver15#FactorsThatDelayTruncation). You can free up the disk space by [Shrinking the log file](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-shrinkfile-transact-sql?view=sql-server-ver15#shrinking-a-log-file-to-a-specified-target-size). Sometimes you need to back up and shrink a transaction log **multiple times** because the logical log file located at the end of the file might be in use. 

  * If you're using features such **Replication Mirroring, Availability groups**, check database mirroring status, which is always displayed on the Dashboard. Also check if the log reader is running or stuck, to understand how much data is pending to be synced on the mirror/Secondary replica. Based on your findings, you can remove the secondary node/replica from Mirroring/AG and [re-add it with a fresh backup of data/log file](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/manually-prepare-a-secondary-database-for-an-availability-group-sql-server?view=sql-server-ver15#SSMSProcedure). 

   * If you're using **CDC (Change Data Capture)**, you can try to disable CDC, do a log backup and [shrink the log.](https://docs.microsoft.com/sql/relational-databases/databases/shrink-a-file?view=sql-server-ver15&viewFallbackFrom=sql-server-ver15). 

   * **Make sure you configure log backup for your databases** frequently so that the log doesn't bloat again. 

* **Extend disk if you're running out of space**  

   You can extend your disk from [Storage Configuration](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#existing-vms), or you can use the [**Disks** blade on Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks) if you're running out of space.  

* **Move database/log file to a different disk/location** 

   If you want to move your database/log file to a different drive, [follow this TSQL](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-file-and-filegroup-options?view=sql-server-ver15#f-moving-a-file-to-a-new-location). After you've run the TSQL, make sure you stop the SQL instance and move the files manually to that location and start SQL Service again. 

* **TempDB not releasing space after shrinking** 

   * Check for long-running sessions and whether there are any temporary tables not dropped. SQL Server drops the temporary table when the connection is closed. Alternately, you can manually remove them by using **Drop Table** in the connection where the temporary table was created. 

   * Check for open transactions and see if they can be stopped, or change the application code if the transactions are not closed. 

## **Recommended Documents** 

* [Shrinking log file](https://www.translatetheweb.com/?from=&to=en&dl=en&ref=trb&a=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Farchive%2Fblogs%2Fjpsql%2Fhowto-management-studio-ldf) 

* [How to manage the size/growth of transaction log](https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file?view=sql-server-ver15) 

* [Create partitioned tables and indexes](https://docs.microsoft.com/sql/relational-databases/partitions/create-partitioned-tables-and-indexes?view=sql-server-ver15) 

* [My drive is full and I want to know what's taking up space](https://windirstat.net/) 

* [Transaction log truncation](https://docs.microsoft.com/sql/relational-databases/logs/the-transaction-log-sql-server?redirectedfrom=MSDN&view=sql-server-ver15#Truncation)
