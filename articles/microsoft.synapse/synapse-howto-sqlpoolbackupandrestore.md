<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738816"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "How-To/SQL pool Backup and Restore"
	description = "How-To/SQL pool Backup and Restore"
	articleId = "synapse-howto-sqlpoolbackupandrestore"
	authors = "saltug"
	ms.author = "saltug"
/>

# How-To/SQL pool Backup and Restore

## **Recommended Steps**

SQL Data Warehouse automatically takes snapshots of your data warehouse so that you can recover from outages and user errors. This will allow you to restore a data warehouse to a previous point in time, restore a deleted data warehouse, or recover from a data center outage. After the data warehouse is restored, make sure you go through the checklist of finalization tasks before you put a newly recovered SQL Data Warehouse back into production.

Follow the links to:

* Restore a deleted data warehouse using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-powershell)
* Restore an active or paused data warehouse using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-powershell)
* Create a [user-defined restore point using Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#create-a-user-defined-restore-point-using-the-azure-portal)
* [Copy your data warehouse with user-defined restore points using PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#create-a-user-defined-restore-point-using-the-azure-portal)
* See information about backup and restore in SQL Data Warehouse, query [sys.pdw_loader_backup_runs](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-pdw-loader-backup-runs-transact-sql?view=aps-pdw-2016-au7)
* See [checklist](https://docs.microsoft.com/azure/sql-database/sql-database-disaster-recovery#configure-your-database-after-recovery) of tasks to properly configure connectivity to your restored data warehouse

## **Recommended Documents**

* [More about backup and restore](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-restore-database-overview/)

