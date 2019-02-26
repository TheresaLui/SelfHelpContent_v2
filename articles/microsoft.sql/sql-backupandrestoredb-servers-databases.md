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
	articleId="18a8e32f-201c-4ccd-ae0d-5b3ec11d7676"
/>

# Backing up and restoring databases

## **Recommended Steps**

SQL Database keeps replicas of your database so that you can recover from outages and user errors. This includes restoring a database to a previous point in time, restoring a deleted database, or recovering from a data center outage. Available options depend on the database service tier and options you chose. After the database is restored, make sure you go through the checklist of finalization tasks before you put a newly recovered Azure SQL Database back into production.

* To restore a database to a previous point in time, click "Restore" at the top of the resource blade for your selected SQL database to open the "Restore" blade, and then fill in the necessary details
* To restore an accidentally deleted database, click the "Deleted Databases" tile at the bottom of your SQL server resource blade under "Operations" to start the restore process.
* To restore as a new database from a geo-redundant backup (also called as Geo-restore), click "New",  "Data and Storage", "SQL Database," then select "Backup" in the source list.
* To [finalize your restored database](https://azure.microsoft.com/documentation/articles/sql-database-recovered-finalize/)
* [To restore a single table from an Azure SQL Database backup](https://docs.azure.cn/sql-database/sql-database-cloud-migrate-restore-single-table-azure-backup/)

## **Recommended Documents**

* [Restore a database to a previous point in time, restore a deleted database, or recover from a data center outage](https://docs.azure.cn/sql-database/sql-database-troubleshoot-backup-and-restore/)<br>
* [Business Continuity Overview](https://docs.azure.cn/sql-database/sql-database-business-continuity/)<br>
* [Design for business continuity](https://azure.microsoft.com/documentation/articles/sql-database-business-continuity-design/)
