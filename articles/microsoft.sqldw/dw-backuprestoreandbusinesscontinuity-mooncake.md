<properties
	pageTitle="How to recover from a backup and data protection"
	description="How to recover from a backup and data protection"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds=""
	productPesIds=""
	displayOrder="3"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-backuprestoreandbusinesscontinuity-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>
# How to recover from a backup and data protection

## **Recommended Steps**
SQL Data Warehouse automatically takes snapshots of your data warehouse so that you can recover from outages and user errors. This will allow you to restore a data warehouse to a previous point in time, restore a deleted data warehouse, or recover from a datacenter outage. After the data warehouse is restored, make sure you go through the checklist of finalization tasks before you put a newly recovered SQL Data Warehouse back into production.

Follow the links to:

* restore a deleted data warehouse using [Azure Portal](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-the-azure-portal) or [PowerShell](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-powershell)
* restore an active or paused data warehouse using [Azure Portal](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-the-azure-portal) or [PowerShell](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-powershell).
* create a [user-defined restore point using Azure Portal](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#create-a-user-defined-restore-point-using-the-azure-portal)
* [copy your data warehouse with user-defined restore points using PowerShell](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#create-a-user-defined-restore-point-using-the-azure-portal)
* see information about back up and restore in SQL Data Warehouse, query [sys.pdw_loader_backup_runs](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-pdw-loader-backup-runs-transact-sql?view=aps-pdw-2016-au7)
* see [checklist](https://docs.azure.cn/sql-database/sql-database-disaster-recovery#configure-your-database-after-recovery) of tasks to properly configure connectivity to your restored data warehouse

## **Recommended Documents**

* [More about back up and restore](https://docs.azure.cn/sql-data-warehouse/backup-and-restore)
