<properties
	pageTitle="Migrating to Azure|Planning a migration"
	description="Migrating to Azure|Planning a migration"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637291"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="3c56c281-38de-48d5-a076-d497a6fc2a71"
	ownershipId="AzureData_AzureSQLMI"
/>

# Planning a migration

Migrating to managed instance can be performed offline and online for most of the workloads. Note that managed instance is nearly 100% compatible with on-prem. SQL server, however there also exists disparity in some of the functionalities supported. For details on managed instance compatibility with on-prem. SQL server please see [Managed instance differences, limitations and known issues](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information).

## **Recommended Steps**

Migration should be approached in several phases: First, assess compatibility of your on-premises SQL databases you wish to migrate to managed instance. Remove any blockers based on the assessment provided. Migrate to managed instance choosing one of the online or offline methods.

**Pre-assessment**

1. Review the list of [Managed instance differences, limitations, and known issues](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information)

**Assessment**

1. Download and run [Data migration assistant](https://docs.microsoft.com/sql/dma/dma-overview?view=sql-server-2017) tool on-premises with your SQL server to automatically assess compatibility of your on-premises databases migrating to managed instance
2. Address any issues indicated by the assessment provided in Data migration assistant
3. In case you have addressed issues, re-run Data migration assistant to ensure your databases are ready for migration

**Migrate many databases online, or offline**

In case you have considerable number of databases to migrate, consider using Data migration service as it automates this process for you allowing minimum downtime. The service needs to be configured to connect with your on-premises systems:

1. Use [Data migration service](https://docs.microsoft.com/azure/dms/tutorial-sql-server-managed-instance-online) to run online migration of your databases following instructions provided

**Migrate single database, offline**

In case you need to migrate a single (or a few) databases offline, the quickest method is to use SQL native backup and restore:

1. Execute native backup of your database with on-prem SQL server
2. Use [restore](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started-restore) to restore your backup database to managed instance

For all methods migrating to managed instance, such is for example transactional replication, see [SQL Database migration methods](https://docs.microsoft.com/azure/sql-database/sql-database-features#migration-methods).

## **Recommended Documents**

- [SQL Database migration methods](https://docs.microsoft.com/azure/sql-database/sql-database-features#migration-methods)
- [Data migration assistant](https://docs.microsoft.com/sql/dma/dma-overview?view=sql-server-2017)
- [Database migration service](https://docs.microsoft.com/azure/dms/tutorial-sql-server-managed-instance-online)
- [Restore a database to a managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started-restore)
