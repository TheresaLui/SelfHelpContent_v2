<properties
	pageTitle="How to recover from a backup"
	description="How to recover from a backup"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="datawarehouse"
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# How to recover from a backup

## **Recommended steps**
SQL Data Warehouse automatically takes snapshots of your data warehouse so that you can recover from outages and user errors.  This will allow you to restore a data warehouse to a previous point in time, restore a deleted data warehouse, or recover from a datacenter outage.  After the data warehouse is restored, make sure you go through the checklist of finalization tasks before you put a newly recovered SQL Data Warehouse back into production.

1. To restore a data warehouse, go to the Azure portal page for the Data Warehouse, open the "Restore blade" and fill in necessary details.
2. To restore a deleted data warehouse, click the "Deleted Databases" tile at the bottom of your SQL Server restore blade under "Operations" to start the restore process.

## **Recommended documents**
[Finalize your restored database](https://azure.microsoft.com/documentation/articles/sql-database-recovered-finalize/)<br>
[More about data protection](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore-database-overview/)
