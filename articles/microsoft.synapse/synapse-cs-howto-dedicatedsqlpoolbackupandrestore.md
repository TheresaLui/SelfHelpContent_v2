<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783860"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "How-To/Dedicated SQL pool - Backup and Restore"
    description = "How-To/Dedicated SQL pool - Backup and Restore"
    articleId = "synapse-cs-howto-dedicatedsqlpoolbackupandrestore.md"
    ms.author = "saltug"
/>

# How-To/Dedicated SQL pool - Backup and Restore

## **Recommended Steps**

Dedicated SQL pool automatically takes snapshots of your Dedicated SQL pool so that you can recover from outages and user errors. This will allow you to restore a Dedicated SQL pool to a previous point in time, restore a deleted Dedicated SQL pool, or recover from a data center outage. After the Dedicated SQL pool is restored, make sure you go through the checklist of finalization tasks before you put a newly recovered Dedicated SQL pool back into production.

Follow the links to:

* Restore a deleted Dedicated SQL pool using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-powershell)

* Restore an active or paused Dedicated SQL pool using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-powershell)

* Create a [user-defined restore point using Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#create-a-user-defined-restore-point-using-the-azure-portal)

* [Copy your Dedicated SQL pool with user-defined restore points using PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#create-a-user-defined-restore-point-using-the-azure-portal)

* See information about backup and restore in Dedicated SQL pool, query [sys.pdw_loader_backup_runs](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-pdw-loader-backup-runs-transact-sql?view=aps-pdw-2016-au7)

* See [checklist](https://docs.microsoft.com/azure/sql-database/sql-database-disaster-recovery#configure-your-database-after-recovery) of tasks to properly configure connectivity to your restored Dedicated SQL pool

## **Recommended Documents**

* [More about backup and restore](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-restore-database-overview/)

 