<properties
	pageTitle="backup/restore/long-term backup retention"
	description="backup/restore/long-term backup retention"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630432"
	productPesIds="13491"
	cloudEnvironments="public"
	articleId="fe65a0a8-b9e5-4a2c-8f94-aa5cf5dc158a"
/>

# backup/restore/long-term backup retention

SQL Database can be configured to retain weekly, monthly, and yearly backups beyond the automated backup retention period to suit regulatory, compliance, or other business purposes via [Long-term backup retention (LTR)](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-long-term-retention)

## **Recommended Steps**
You can [manage LTR for your database](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure) via the Azure Portal, PowerShell, or the REST API to:

* Change policy configuration:
  * Weekly backup retention
  * Monthly backup retention
  * Yearly backup retention
  * Week of year for yearly backup
* View backups
* Restore from a backup
* Delete backups

## **Recommended Documents**

* [**Automated backups and point in time restore (PITR)**](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?WT.mc_id=pid:13491:sid:32630409/): SQL Database automatically creates database backups that can be used to restore a database to any point in time within the backup retention period