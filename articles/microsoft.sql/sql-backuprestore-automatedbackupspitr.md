<properties
	pageTitle="backup/restore/automated backups or point in time restore"
	description="bbackup/restore/automated backups or point in time restore"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630409"
	productPesIds="13491"
	cloudEnvironments="public"
	articleId="eeb46dff-62eb-4d87-b7a9-939908fc69df"
/>

# backup/restore/automated backups or point in time restore


## **Recommended steps**
SQL Database automatically creates database backups that can be used to restore a database to any point in time within the backup retention period.

### **Automated Backups**

* No configuration or setup is required to start taking automated backups
* [Backup scheduling](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409/#how-often-do-backups-happen) is handled transparently and is dependent on compute size and database activity <br>
  * Transaction log backups are generally taken every 5-10 minutes
  * Differential database backups generally occur every 12 hours
  * Full database backups are created once a week
* [You can change the backup retention period](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409/#how-to-change-the-pitr-backup-retention-period) for a database to 7, 14, 21, 28, or 35 days via the Azure Portal, PowerShell, or the REST API <br>
  * The default retention period for Standard and Premium databases is 35 days (5 weeks)
  * The default retention period for Basic and vCore-based databases is 7 days
* You cannot view a list of automated backups due to their frequency and nature <br>
  * Automated backups will cover the entire range of times within the backup retention period
  * [Long-term retention backups can be listed](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure?WT.mc_id=pid:13491:sid:32630409/#view-backups-and-restore-from-a-backup-using-azure-portal) and should not be confused with automated backups for point in time restore

### **Restore**

* The following options are available for [restoring databases from automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups?WT.mc_id=pid:13491:sid:32630409/): <br>
  * Create a new database on the same SQL Database server recovered to a specified point in time within the retention period
  * Create a database on the same SQL Database server recovered to the deletion time for a deleted database
  * Create a new database on any SQL Database server in the same region recovered to the point of the most recent backups
  *  Create a new database on any SQL Database server in any other region recovered to the point of the most recent replicated backups
* Restoring a database can't directly replace an original database, however, you can rename the databases after the restore completes

## **Recommended documents**

* [**Long-term backup retention (LTR)**](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-retention?WT.mc_id=pid:13491:sid:32630409/): SQL Database can be configured to retain weekly, monthly, and yearly backups beyond the automated backup retention period to suit regulatory, compliance, or other business purposes
* [**Geo-restore**](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups?WT.mc_id=pid:13491:sid:32630409/#geo-restore): SQL Databases can be restored on any server in any Azure region from the most recent geo-replicated backup