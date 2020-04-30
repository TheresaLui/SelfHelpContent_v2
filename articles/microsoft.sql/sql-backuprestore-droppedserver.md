<properties
	pageTitle="backup/restore/recover dropped server or resource group"
	description="backup/restore/recover dropped server or resource group"
	service="microsoft.sql"
	resource="servers"
	authors="KeithJH"
	ms.author="keithor"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630451"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="cd7113bd-0d84-4617-9420-416b7f09bbc5"
	ownershipId="AzureData_AzureSQLDB_BackupRestore"
/>

# Backup/restore/recover dropped server or resource group

If you delete an Azure SQL Database server, all databases are also deleted and cannot be recovered. There is currently no support for restoring a deleted server.

To learn how to avoid business interruptions you can review the capabilities that Azure SQL Database provides for [business continuity](https://docs.microsoft.com/azure/sql-database/sql-database-business-continuity?WT.mc_id=pid:13491:sid:32630451/).

## **Recommended Steps**

Check if the databases under the server can be recovered using supported features:

* If the server still exists you can [restore deleted databases](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups?WT.mc_id=pid:13491:sid:32630451#deleted-database-restore) from the Azure portal, PowerShell, or REST APIs
* If [long-term backup retention](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-retention?WT.mc_id=pid:13491:sid:32630451/) was enabled for the databases you can [restore from long-term backups](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure?WT.mc_id=pid:13491:sid:32630451/)
* If [geo-replication](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication?WT.mc_id=pid:13491:sid:32630451/) was enabled for the databases another copy of the databases may be running under a different server

An attempt to recover a server via a support request will have the best chances if:

* A server with the same name has not been created
* The server was dropped less than 7 days ago
