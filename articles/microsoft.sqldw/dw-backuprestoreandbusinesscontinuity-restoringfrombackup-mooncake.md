<properties
    pageTitle="Restoring from backup"
    description="Restoring from backup"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds=""
    productPesIds=""
    displayOrder="2"
    selfHelpType="resource"
    resourceTags="datawarehouse"
    articleId="dw-backuprestoreandbusinesscontinuity-restoringfrombackup-mooncake"
    cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>

# Restoring from backup

## **Recommended Steps**

* If you are trying to restore a data warehouse from a backup:

  * restore a deleted data warehouse using [Azure Portal](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-the-azure-portal) or [PowerShell](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-powershell)
  * restore an active or paused data warehouse using [Azure Portal](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-the-azure-portal) or [PowerShell](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-powershell).  Note that when restoring, you can specify a different ServiceObjectiveName (DWU) or a different server residing in a different region.
  * If portal doesn’t show restore point, use [PowerShell](https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaserestorepoint?view=azps-2.4.0#examples) to confirm if the restore point was created

* If you are moving or restoring your data warehouse across subscriptions:

  * Go through the [checklist](https://docs.azure.cn/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources) before moving your data warehouse across subscriptions
  * If you need to 'restore' with a new data warehouse across subscriptions, follow the instructions on restoring and using the Move functionality [here](https://docs.azure.cn/sql-data-warehouse/backup-and-restore#restoring-from-restore-points)

* If you are restoring the data warehouse to a different server, follow this [checklist](https://docs.azure.cn/sql-database/sql-database-disaster-recovery#configure-your-database-after-recovery) to ensure recovered data warehouse has appropriate security configuration.

  * To re-map a database user to a different login, use ```ALTER USER <UserName> WITH LOGIN = <LoginName>```

## **Recommended Documents**

* Overview of [back up and restore](https://docs.azure.cn/sql-data-warehouse/backup-and-restore)
* Understanding [restore points](https://docs.azure.cn/sql-data-warehouse/backup-and-restore#restoring-from-restore-points)
* Learn the basics on the Move functionality including how to [automate via PowerShell](https://docs.azure.cn/azure-resource-manager/resource-group-move-resources#use-azure-powershell)
