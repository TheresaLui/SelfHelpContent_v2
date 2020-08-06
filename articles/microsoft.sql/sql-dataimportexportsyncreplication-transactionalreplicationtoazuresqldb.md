<properties
	pageTitle="data import, export, sync, replication/transactional replication to Azure SQL db"
	description="data import, export, sync, replication/transactional replication to Azure SQL db"
	service="microsoft.sql"
	resource="servers"
	authors="mravikiran"
    ms.author="mravikiran"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630458"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="3b871e6b-d8d8-4a10-9f46-690779769518"
	ownershipId="AzureData_AzureSQLDB"
/>

# REPLICATION

[Replication](https://docs.microsoft.com/sql/relational-databases/replication/sql-server-replication?view=sql-server-2017) is a set of technologies for copying and distributing data and database objects from one database to another and then synchronizing between databases to maintain consistency. Following recommendations are for [Transactional Replication](https://docs.microsoft.com/sql/relational-databases/replication/transactional/transactional-replication?view=sql-server-2017).

## **Recommended Steps**

1. If transactional replication appears to be slow and the subscriber is in Azure SQL Database: 

    * Scale the SQL Database to a premium pricing tier. You can change [DTU service tiers](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu) or [vCore characteristics](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases) at any time with minimal downtime to your application (generally averaging under four seconds). It is suggested that you pause all workload before you scale to avoid rollbacks.
    * To optimize costs, you could scale up before the replication process starts and then scale back down after it’s completed

2. If the replication is failing with a timeout error, customer can re-try replication by increasing the querytimeout:

    * Please open the distributor and log reader job properties from Job activity monitor for respective publication
    * Right click on Distributor Job and select properties
    * Go to Step
    * Click on second step of job and click on edit
    * Add parameter -QueryTimeOut 3600 at the end of command (time is in seconds)
    * After increasing the querytimeout you have to restart distribution and logreader agent job from job activity monitor

3. Error 2627 - Violation of PRIMARY KEY(PK) constraint. Cannot insert duplicate key in object:

    * You may try to delete the row with PK (at the Subscriber). The distribution agent will then be able to insert the row again into the subscriber table.
    * Another option would be to configure the Distribution Agent with the SkipErrors parameters. This has the disadvantage though that the failed insert will be ignored; the data on Publisher and Subscriber might become different then.

4. To add new article to existing publication without generating a new snapshot, please disable below 2 properties of publication:

    * Allow_Anonymous : `EXEC sp_changepublication @publication = '<yourpublicationname>', @property = N'allow_anonymous', @value = 'false'`
    * Immediate_Sync : `EXEC sp_changepublication @publication = '<yourpublicationname>’, @property = N'immediate_sync', @value = 'false'`

## **Recommended Documents**

* [Types of Replication](https://docs.microsoft.com/sql/relational-databases/replication/types-of-replication?view=sql-server-2017)
* [Prepare Server for Replication](https://docs.microsoft.com/sql/relational-databases/replication/tutorial-preparing-the-server-for-replication?view=sql-server-2017)
* [Configure Transactional Replication](https://docs.microsoft.com/sql/relational-databases/replication/tutorial-replicating-data-between-continuously-connected-servers?view=sql-server-2017)
* [For monitoring Replication](https://docs.microsoft.com/sql/relational-databases/replication/monitor/monitoring-replication?view=sql-server-2017)

### Notes

* As an alternative to Transactional replication, you can synchronize databases by using [SQL Data Sync](https://docs.microsoft.com/azure/sql-database/sql-database-sync-data)  

