<properties
	pageTitle="Issues with SQL Database backup, restore, automated backups or point in time restore"
	description="Issues with SQL Database backup, restore, automated backups or point in time restore"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
	ms.author="andikshi"
	displayOrder="3"
	selfHelpType="generic"
	supportTopicIds="32688667"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
	resourceTags="servers, databases"
	articleId="sqldb-selfhelp-solutions-backuprestore-automatedbackups"
	ownershipId="AzureData_AzureSQLDB_BackupRestore"
/>

# Issues with SQL Database backup, restore, automated backups or point in time restore

## **Recommended Steps**

SQL Database automatically creates database backups that can be used to restore a database to any point in time within the backup retention period.

### **Automated Backups**

* No configuration or setup is required to start taking automated backups
* [Backup scheduling](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409/#how-often-do-backups-happen) is handled transparently and is dependent on compute size and database activity:

	* Transaction log backups are generally taken every 5-10 minutes
	* Differential database backups generally occur every 12 hours
	* Full database backups are created once a week

* There are [storage costs](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409#storage-costs) associated for backups retained for vCore databases. The backup cost depends on the size of the database, the rate of change and the configured retention period. The backup storage amount equal to the database size is provided at no extra charge. The [pricing page](https://azure.microsoft.com/pricing/details/sql-database/single/) can be used to find region specific pricing and more details.

	* You can gain more insight into the storage space used by viewing the backup [metrics](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported?WT.mc_id=pid:13491:sid:32630409#microsoftsqlserversdatabases) for your database. Large diff/log backup storage sizes indicate a high rate of change of data while large full backup storage sizes indicate a large amount of data.
	* Typically to reduce backup storage costs you will reduce the backup retention period

* [You can change the backup retention period](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409/#how-to-change-the-pitr-backup-retention-period) for a database to 1-35 days via the Azure Portal, PowerShell, or the REST API:

	* The default retention period for databases is 7 days
	* Basic tier databases have a maximum retention of 7 days

* You cannot view a list of automated backups:

	* Automated backups will cover the entire range of times within the backup retention period
	* [Long-term retention backups can be listed](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure?WT.mc_id=pid:13491:sid:32630409/#view-backups-and-restore-from-a-backup-using-azure-portal) and should not be confused with automated backups for point in time restore<br>
