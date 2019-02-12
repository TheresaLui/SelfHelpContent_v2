<properties
	pageTitle="Migrating between servers or subscriptions, or to and from Azure"
	description="Migrating between servers or subscriptions, or to and from Azure"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="31980413"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
	articleId="2cc40ccd-4391-45c2-a121-bcf1af1fc564"
/>

# Migrating between servers or subscriptions, or to and from Azure

## **Recommended Steps**

The following details explain how to migrate or move databases:

* To move a database to a different server in the same subscription, click "Copy" at the top of the SQL database resource blade
* To move the logical server between subscriptions, click "Move" at the top of the SQL server resource blade that hosts your database, then pick resources to move and the subscription to move to. Note: Database cannot be moved between subscriptions directly.<br>
* To [migrate a SQL Server database to Azure SQL](https://docs.azure.cn/sql-database/sql-database-cloud-migrate/), first run the compatibility tool to determine whether it can be migrated, fix any incompatibility issues and then select an appropriate migration method.<br>
* Create a copy of a database so it can be used outside of Azure, [Export a BACPAC file](https://docs.azure.cn/sql-database/sql-database-export/).

## **Recommended Documents**

* [Move databases between servers, between subscriptions, and into and out of Azure](https://docs.azure.cn/sql-database/sql-database-troubleshoot-moving-data/)<br>
* [How to copy an Azure SQL database](https://docs.azure.cn/sql-database/sql-database-troubleshoot-moving-data/)
