<properties
    pageTitle="Understanding automated backups"
    description="Understanding automated backups"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635224"
    productPesIds="15818"
    displayOrder="71"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-backuprestoreandbusinesscontinuity-understandingautomatedbackup.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Troubleshooting automated backups

## **Recommended Steps**

* Azure SQL Data Warehouse takes a snapshot of your data warehouse every 8 hours
* You can restore the data warehouse from any one of snapshots taken
* The user doesn't have to enable this capability
* Automatic restore points are available for 7 days. If you require restore points longer than 7 days, please vote for this capability [here](https://feedback.azure.com/forums/307516-sql-data-warehouse/suggestions/35114410-user-defined-retention-periods-for-restore-points).
* Automatic restore points can't be deleted by the user. SQL Data Warehouse deletes a restore point when it hits the 7-day retention period and when there are at least 42 restore points (user-defined as well as automatic).
Snapshots are not taken when the data warehouse is paused.
* If a snapshot is taken and the data warehouse is paused for more than 7 days and then resumed, it is possible for the restore point to persist longer than 7 days until there are 42 total restore points. Backups don't occur when the data warehouse is paused so the storage cost for backup should remain constant during this time.

## **Recommended Documents**

* [More details about backup and restore in SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-points)
* [How to create restore points](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-points)
