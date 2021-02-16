<properties
	pageTitle="backup/restore/restore"	
	description="backup/restore/restore"
	service="microsoft.sql"	
	resource="servers"	
	authors="sojaga"	
	ms.author="sojaga"	
	displayOrder=""	
	selfHelpType="generic"	
	supportTopicIds="32688668"	
	productPesIds="13491"	
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"	
	articleId="f39fd2ea-00d9-4c05-a271-35611754ad1c"	
	ownershipId="AzureData_AzureSQLDB_BackupRestore"	
/>

# backup/restore/restore

## **Recommended Steps**

**Point-in-Time Restore**

* The following options are available for [point-in-time restore](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups?WT.mc_id=pid:13491:sid:32688668/) of databases from automated backups:

	* Create a new database on the same SQL Database server recovered to a specified point in time within the retention period
	* Create a database on the same SQL Database server recovered to the deletion time for a deleted database

* Restoring a database does not replace the existing source database. You can, however, rename the original and restored databases.

**Geo-Restore**

[Geo-restore](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups?WT.mc_id=pid:13491:sid:32688668/#geo-restore) uses a geo-replicated backup and can be requested even if the database or data center is inaccessible due to an outage. You can restore the database to a server in any other region. There is a delay between when a backup is taken and when it is geo-replicated to an Azure blob in a different region, so the geo-restored database can contain older data than the latest point in time restore in the same region.

## **Recommended Steps**

* **No backups were found to restore the database to the point in time \<time\> (UTC). Please contact support to restore the database.**

  * If the exact point in time requested isn't necessary, you can attempt to restore to a later point in time, particularly if the requested time is close to database creation time.
  * When databases are configured for [active geo-replication](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication?WT.mc_id=pid:13491:sid:32688668), only the geo-primary database generates backups. If the requested database was geo-secondary during the requested point in time, you can attempt the restore from the geo-primary database.

* **Database '\<database name\>' already exists. Choose a different database name.**

  * Restoring a database does not replace the existing source database. You can, however, rename the original and restored databases.

* **The restored database is too large for \<target edition\> edition. Specify a target edition with sufficient storage.**

  * If you do not explicitly specify a target service objective, the restored database will take the service objective that the source database currently is. This may not support the size of the source database at the requested point in time, so you'll need to explicitly specify a target service objective that does.
  * If you are specifying a target service objective that should support the database size, you can first attempt the restore to a higher service objective and scale the database down after restore has completed.

* **No error but restore is taking longer than expected**

  * Restore operations are resource intensive, and are a size-of-data operation. To get better performance, you can restore to a higher service objective and scale the database down after restore has completed.
  * If you are restoring into an elastic pool, you'll get the best performance if you limit the number of concurrent restores into the same pool.

* **I want to restore an existing `.bak`file**

  * Single Azure SQL databases and elastic pools do not allow restoring from provided `.bak` files. We recommend using [.Bacpac files for importing](https://docs.microsoft.com/azure/sql-database/sql-database-export?WT.mc_id=pid:13491:sid:32688668).
  * Azure SQL Database Managed instance does support [native restore](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started-restore?WT.mc_id=pid:13491:sid:32688668) from .bak files

## **Recommended Documents**

* [Disaster recovery using geo-restore](https://docs.microsoft.com/azure/sql-database/saas-dbpertenant-dr-geo-restore?WT.mc_id=pid:13491:sid:32688668/)<br>
