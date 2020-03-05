<properties
	pageTitle="data import, export, sync, replication/copy database within Azure"
	description="data import, export, sync, replication/copy database within Azure"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32630415"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
    resourceTags="servers, databases"
	articleId="sql-dataimportexportsyncreplication-copydatabasewithinazure-mooncake"
	ownershipId="AzureData_AzureSQLDB"
/>

# data import, export, sync, replication/copy database within Azure

## **Recommended Steps**

The following details explain how to migrate or move database.

* To move a database to a different server in the same subscription, click "Copy" at the top of the SQL database resource blade.
* To move the logical server between subscriptions, click "Move" at the top of the SQL server resource blade that hosts your database, then pick resources to move and the subscription to move to. Note: Databases cannot be moved between subscriptions directly.
* To [migrate an SQL Server database to Azure SQL](https://docs.azure.cn/sql-database/sql-database-single-database-migrate), first run the compatibility tool to determine whether it can be migrated, fix any incompatibility issues, then select an appropriate migration method.
* Create a copy of a database so it can be used outside of Azure: [Export a BACPAC file](https://docs.azure.cn/sql-database/sql-database-export)

## **Recommended Documents**

* [Move databases between servers, between subscriptions, and into and out of Azure](https://docs.azure.cn/sql-database/sql-database-technical-overview)
* [How to copy an Azure SQL database](https://docs.azure.cn/sql-database/sql-database-technical-overview)
