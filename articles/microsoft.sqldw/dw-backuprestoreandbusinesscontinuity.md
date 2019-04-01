<properties
	pageTitle="How to recover from a backup and data protection"
	description="How to recover from a backup and data protection"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635177, 32635201, 32635207, 32635215, 32635218, 32635224"
	productPesIds="15818"
	displayOrder="107"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-backuprestoreandbusinesscontinuity.md"
	cloudEnvironments="public"
/>
# Backup, Restore and Business Continuity

## **Recommended Steps**
SQL Data Warehouse automatically takes snapshots of your data warehouse so that you can recover from outages and user errors. This will allow you to restore a data warehouse to a previous point in time, restore a deleted data warehouse, or recover from a datacenter outage. After the data warehouse is restored, make sure you go through the checklist of finalization tasks before you put a newly recovered SQL Data Warehouse back into production.

* [Restore a deleted database](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-database-portal#restore-a-deleted-database)

## **Recommended Documents**
* [Finalize your restored database](https://azure.microsoft.com/documentation/articles/sql-database-recovered-finalize/)<br>
* [More about data protection](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-restore-database-overview/)