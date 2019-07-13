<properties
    pageTitle="Restoring from backup"
    description="Restoring from backup"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635218"
    productPesIds="15818"
    displayOrder="71"
    selfHelpType="resource"
    resourceTags="datawarehouse"
    articleId="dw-backuprestoreandbusinesscontinuity-restoringfrombackup.md"
    cloudEnvironments="public"
/>

# Restoring from backup

## **Recommended Steps**

* If you are trying to restore a data warehouse from a backup

  * restore a deleted data warehouse using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-a-deleted-database-using-powershell)
  * restore an active or paused data warehouse using [Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-the-azure-portal) or [PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore#restore-an-active-or-paused-database-using-powershell)
  * If portal doesn’t show restore point, use [PowerShell](https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaserestorepoint?view=azps-2.4.0#examples) to confirm if the restore point was created.

* If you are moving or restoring your data warehouse across subscriptions

  * Go through the [checklist](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources) before moving your data warehouse across subscriptions
  * If you need to 'restore' with a new data warehouse across subscriptions, follow the instructions on restoring and using the Move functionality [here](https://docs.microsoft.com/azure/sql-data-warehouse/backup-and-restore#restoring-from-restore-points)

## **Recommended Documents**

* Overview of [back up and restore](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-restore-database-overview/)
* Understanding [restore points](https://docs.microsoft.com/azure/sql-data-warehouse/backup-and-restore#restoring-from-restore-points)
* Learn the basics on the Move functionality including how to [automate via PowerShell](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#use-azure-powershell)
