<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783871"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Administration and Security/Dedicated SQL pool - Restoring from backup"
    description = "Administration and Security/Dedicated SQL pool - Restoring from backup"
    articleId = "synapse-cs-administrationandsecurity-dedicatedsqlpoolrestoringfrombackup.md"
    ms.author = "saltug"
/>

# Administration and Security/Dedicated SQL pool - Restoring from backup

## **Recommended Steps**

* Create user-defined restore points via [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-points#create-user-defined-restore-points-through-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-points)

* If you are trying to restore a Dedicated SQL pool from a backup:

	* Restore a deleted Dedicated SQL pool using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-deleted-dw#restore-a-deleted-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-deleted-dw#restore-a-deleted-data-warehouse-through-powershell)

	* Restore an active or paused Dedicated SQL pool using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-active-paused-dw#restore-an-existing-data-warehouse-through-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-active-paused-dw#restore-an-existing-data-warehouse-through-powershell). Note that when restoring, you can specify a different ServiceObjectiveName (DWU) or a different server residing in a different region.

	* If portal doesn?t show restore point, use [PowerShell](https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaserestorepoint?view=azps-2.4.0#examples) to confirm if the restore point was created. Please note that the default retention for Synapse Dedicated SQL pools is 7 days.  

	* Restoring a user defined restore point to a different server is currently only supported via [PowerShell](https://docs.microsoft.com/bs-latn-ba/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-restore-active-paused-dw#restore-an-existing-sql-pool-through-powershell).

* If you have recently renamed your Synapse database and you receive the following error when trying to recover a geo-backup:

    "No Geo-Backup has been created yet" (via Portal) 
    
    "NotFound" (via PowerShell)

    This may be because the rename has not been replicated to your regional pair. Customers experiencing this issue can use the old name to recover their Synapse database. 

* If you are trying to restore a geo-backup and are unable to find a restore point, this may be due to frequent pausing of your Dedicated SQL pool. Restore points may not have a chance to complete if the Dedicated SQL pool is frequently paused.

* If you are moving or restoring your Dedicated SQL pool across subscriptions:

	* Go through the [checklist](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources) before moving your Dedicated SQL pool across subscriptions

	* If you need to 'restore' with a new Dedicated SQL pool across subscriptions, follow the instructions [here](https://techcommunity.microsoft.com/t5/Azure-Data-Warehouse-Support/How-To-Move-your-Azure-Data-Warehouse-to-a-new-region-and-or/ba-p/682907)

	* If you are restoring the Dedicated SQL pool to a different server, follow this [checklist](https://docs.microsoft.com/azure/sql-database/sql-database-disaster-recovery#configure-your-database-after-recovery) to ensure recovered Dedicated SQL pool has appropriate security configuration

	* To re-map a database user to a different login, use ```ALTER USER <UserName> WITH LOGIN = <LoginName>```

* If you receive an error message stating "The server is not in a ready state", check the status of the destination SQL Server to ensure that it is in an "Available" state. The status can be found in the Overview pane of the destination SQL Server in the Azure Portal.

* Please note that Synapse Analytics Dedicated SQL pools do not currently support table level restores. It is only possible to recover an entire database from your backup. 

## **Recommended Documents**

* Overview of [backup and restore](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-restore-database-overview/)

* Understanding [restore points](https://docs.microsoft.com/azure/sql-data-warehouse/backup-and-restore#restoring-from-restore-points)

* Learn the basics on the Move functionality including how to [automate via PowerShell](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#use-azure-powershell)

 