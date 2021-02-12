<properties
	pageTitle="backup/restore/long-term backup retention"
	description="backup/restore/long-term backup retention"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32630432"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="fe65a0a8-b9e5-4a2c-8f94-aa5cf5dc158a"
	ownershipId="AzureData_AzureSQLDB_BackupRestore"
/>

# backup/restore/long-term backup retention

SQL Database can be configured to retain weekly, monthly, and yearly backups beyond the automated backup retention period to suit regulatory, compliance, or other business purposes via [long-term backup retention](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-retention?WT.mc_id=pid:13491:sid:32630432/).

## **Recommended Steps**
You can [manage long-term backup retention for your database](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure?WT.mc_id=pid:13491:sid:32630432/) via the Azure Portal, PowerShell, or the REST API to:

* Change policy configuration, including:

  * How long to keep weekly backups
  * How long to keep the first backup of each month
  * Which weekly backup of the year to take for annual backups
  * How long to keep annual backups

* View backups
* Restore from backups
* Delete backups

## **Recommended Documents**

* [**Automated backups and point in time restore (PITR)**](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630432/): SQL Database automatically creates database backups that can be used to restore a database to any point in time within the backup retention period
