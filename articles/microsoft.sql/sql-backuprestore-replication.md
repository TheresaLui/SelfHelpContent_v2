<properties
	pageTitle="Common Solutions Template"
	description="Common Solutions Template"
	infoBubbleText="Common Solutions Template"
	service=""
	resource=""
	authors=""
	ms.author=""
	displayOrder=""
	articleId=""
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments=""
/>

# **REPLICATION**
[Replication](https://docs.microsoft.com/en-us/sql/relational-databases/replication/sql-server-replication?view=sql-server-2017) is a set of technologies for copying and distributing data and database objects from one database to another and then synchronizing between databases to maintain consistency. Following recommendations are for [Transactional Replication](https://docs.microsoft.com/en-us/sql/relational-databases/replication/transactional/transactional-replication?view=sql-server-2017) and Geo-Replication 


## **Transactional Replication**

## **Recommended Steps**

1. If transaction replication appears to be slow and the subscriber is in Azure SQL Database: 
    * Scale the SQL Database to a premium pricing tier. You can change [DTU service tiers](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-service-tiers-dtu) or [vCore characteristics](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-vcore-resource-limits-single-databases)  at any time with minimal downtime to your application (generally averaging under four seconds). 
    * To optimize costs, you could scale up before the replication process starts and then scale back down after it’s completed. 
    * During the upgrade, the database will remain transactionally consistent. It is suggested that you pause all workload before you scale to avoid rollbacks.

2. If the replication is failing with a timeout error. Customer can re-try replication by increasing the querytimeout:
    * Please open the distributor and log reader job properties from Job activity monitor for respective publication.
    * Right click on Distributor Job and select properties
    *  Go to Step
    *  Click on second step of job and click on edit
    *  add parameter -QueryTimeOut 3600 at the end of command
    * After increasing the querytimeout you have to restart distribution and logreader agent job from job activity monitor.

3. Error 2627 - Violation of PRIMARY KEY constraint <>. Cannot insert duplicate key in object 
    * you may try to delete the row with PK *at the Subscriber*. The distribution agent will then be able to insert the row again into the subscriber table
    * Another option would be to configure the Distribution Agent with the SkipErrors parameters. This has the disadvantage though that the failed insert will be ignored; the data on Publisher and Subscriber might become different then.

4. To add new article to existing publication without generating a new snapshot, please disable below 2 properties of publication:
    1. Immediate_sync 
    EXEC sp_changepublication
    @publication = '<yourpublicationname>',
    @property = N'allow_anonymous',
    @value = 'false'
    GO

    2. Allow_anonymous
    EXEC sp_changepublication
    @publication = '<yourpublicationname>’,
    @property = N'immediate_sync',
    @value = 'false'
    GO

```
[cluster my-cluster]
    FormLayout = selectionpanel
    Category = My Templates
    CategoryOrder = 100
    MaxCount = 200
    Autoscale = $Autoscale
```

## **Recommended Documents**

* [Types of Replcation](https://docs.microsoft.com/en-us/sql/relational-databases/replication/types-of-replication?view=sql-server-2017)
* [Prepare Server for Replication](https://docs.microsoft.com/en-us/sql/relational-databases/replication/tutorial-preparing-the-server-for-replication?view=sql-server-2017)
* [Configure Transactional Replication](https://docs.microsoft.com/en-us/sql/relational-databases/replication/tutorial-replicating-data-between-continuously-connected-servers?view=sql-server-2017)
* [For monitoring Replication](https://docs.microsoft.com/en-us/sql/relational-databases/replication/monitor/monitoring-replication?view=sql-server-2017)

## **Geo-Replication**

## **Recommended Documents**

* [Create readable secondary databases using active geo-replication](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication?WT.mc_id=pid:13491:sid:32630424/)<br>
* [Configure active geo-replication in the Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication-portal?WT.mc_id=pid:13491:sid:32630424/)<br>
* [Disaster recovery using database geo-replication](https://docs.microsoft.com/azure/sql-database/saas-dbpertenant-dr-geo-replication?WT.mc_id=pid:13491:sid:32630424/)<br>
* [PowerShell example to configure active geo-replication for a single database](https://docs.microsoft.com/azure/sql-database/scripts/sql-database-setup-geodr-and-failover-database-powershell?toc=%2fpowershell%2fmodule%2ftoc.json?WT.mc_id=pid:13491:sid:32630424/)<br>
* [PowerShell example to configure active geo-replication for a pooled database](https://docs.microsoft.com/azure/sql-database/scripts/sql-database-setup-geodr-and-failover-pool-powershell?toc=%2fpowershell%2fmodule%2ftoc.json?WT.mc_id=pid:13491:sid:32630424/)