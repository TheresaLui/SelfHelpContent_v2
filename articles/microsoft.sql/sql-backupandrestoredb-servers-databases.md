<properties
	pageTitle="Backing up and restoring databases"
	description="Backing up and restoring databases"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32302682"
	resourceTags="databases, servers"
	productPesIds="13491"
	cloudEnvironments="public"
/>

# Backing up and restoring databases

## **Recommended steps**
SQL Database keeps replicas of your database so that you can recover from outages and user errors. This includes restoring a database to a previous point in time, restoring a deleted database, or recovering from a data center outage. Available options depend on the database service tier and options you chose. After the database is restored, make sure you go through the checklist of finalization tasks  before you put a newly recovered Azure SQL Database back into production.

* Restore a database to a previous point in time.<br>
Click "Restore" at the top of the resource blade for your selected SQL database to open the "Restore  blade," and then fill in the necessary details.
* Restore an accidentally deleted database.<br>
Click the "Deleted Databases"  tile at the bottom of your SQL server resource blade under "Operations" to start the restore process.
* Restore as a new database from a geo-redundant backup, which is also called as Geo-restore.<br>
Click "New," click "Data and Storage," click "SQL Database,"  and then select "Backup" in the source list.
* Complete finalization task checklist for a restored database<br>
[Finalize your restored database](https://azure.microsoft.com/documentation/articles/sql-database-recovered-finalize/)
* Restore a single table from Azure database backup.<br>
[How to restore a single table from an Azure SQL Database backup](https://azure.microsoft.com/documentation/articles/sql-database-cloud-migrate-restore-single-table-azure-backup/)

## **Recommended documents**
[Restore a database to a previous point in time, restore a deleted database, or recover from a data center outage](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups)<br>
[Business Continuity Overview](https://azure.microsoft.com/documentation/articles/sql-database-business-continuity/)<br>
[Learn about automatic SQL database backup](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
