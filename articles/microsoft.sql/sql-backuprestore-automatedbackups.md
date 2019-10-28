<properties
	pageTitle="Issues with SQL Database backup, restore, automated backups or point in time restore"
	description="Issues with SQL Database backup, restore, automated backups or point in time restore"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  ms.author="andikshi"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32688667"
	productPesIds="13491"
	cloudEnvironments="public"
    resourceTags="servers, databases"
	articleId="sqldb-selfhelp-solutions-backuprestore-automatedbackups"
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

* [You can change the backup retention period](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409/#how-to-change-the-pitr-backup-retention-period) for a database to 7, 14, 21, 28, or 35 days via the Azure Portal, PowerShell, or the REST API:

	* The default retention period for Standard and Premium databases is 35 days (5 weeks)
	* The default retention period for Basic and vCore-based databases is 7 days

* You cannot view a list of automated backups:

	* Automated backups will cover the entire range of times within the backup retention period
	* [Long-term retention backups can be listed](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure?WT.mc_id=pid:13491:sid:32630409/#view-backups-and-restore-from-a-backup-using-azure-portal) and should not be confused with automated backups for point in time restore<br>
