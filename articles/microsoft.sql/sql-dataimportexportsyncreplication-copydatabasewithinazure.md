<properties
	pageTitle="data import, export, sync, replication/copy database within Azure"
	description="data import, export, sync, replication/copy database within Azure"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder="7"
	selfHelpType="generic"
	supportTopicIds="32630415"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax"
    resourceTags="servers, databases"
	articleId="514fdf6b-b8b0-4887-a734-2236d1907bff"
	ownershipId="AzureData_AzureSQLDB"
/>

# data import, export, sync, replication/copy database within Azure

## **Recommended Steps**

The following details explain how to migrate or move database. <br>

* To move a database to a different server in the same subscription, click "Copy" at the top of the SQL database resource blade.
* To move the logical server between subscriptions, click "Move" at the top of the SQL server resource blade that hosts your database, then pick resources to move and the subscription to move to. Note: Databases cannot be moved between subscriptions directly.<br>
* To [migrate an SQL Server database to Azure SQL](https://azure.microsoft.com/documentation/articles/sql-database-cloud-migrate?WT.mc_id=pid:13491:sid:32630415/), first run the compatibility tool to determine whether it can be migrated, fix any incompatibility issues, then select an appropriate migration method.<br>
* Create a copy of a database so it can be used outside of Azure: [Export a BACPAC file](https://azure.microsoft.com/documentation/articles/sql-database-export?WT.mc_id=pid:13491:sid:32630415/)<br>

## **Recommended Documents**

* [Move databases between servers, between subscriptions, and into and out of Azure](http://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-moving-data?WT.mc_id=pid:13491:sid:32630415/)<br>
* [How to copy an Azure SQL database](http://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-moving-data?WT.mc_id=pid:13491:sid:32630415/)<br>
