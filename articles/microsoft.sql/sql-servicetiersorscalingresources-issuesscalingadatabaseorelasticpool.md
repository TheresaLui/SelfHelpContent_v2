<properties
	pageTitle="SQL Database issues scaling a database or elastic pool"
	description="SQL Database issues scaling a database or elastic pool"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa, johirsch,andikshi"
    ms.author="emlisa,andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630431, 32630452"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="cbfbab1e-05e9-4631-9ef8-e1467611c765"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# SQL Database issues scaling a database or elastic pool

### Scaling Operation Slow or Stuck

Scaling operations can take anywhere from a few minutes to several hours depending on the service tiers involved and sometimes the size of the database.  For information on factors that affect how long a scaling operation runs and rules of thumb for estimating how long a scaling operation should take, see the following.

* [Scaling a single database](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale#change-compute-resources-vcores-or-dtus)<br>
* [Scaling an elastic pool](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale#change-compute-resources-vcores-or-dtus)<br>

### Issues Scaling with Geo-Replication Enabled

If geo-replication is enabled, the sequencing of scaling operations on the primary database and secondary databases is important. To upgrade, scale the secondary databases first. To downgrade, scale the primary database first. For more detail, see the following:

* [Scaling a single database](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale#change-compute-resources-vcores-or-dtus)

## **Recommended Documents**

* [Scalability overview](https://docs.microsoft.com/azure/sql-database/sql-database-scalability-index?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Resources for scaling a single database](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Resources for scaling an elastic pool](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Scale up/down](https://docs.microsoft.com/azure/sql-database/sql-database-scale-resources?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Scaling out with database sharding](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-scale-introduction?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Read scale-out](https://docs.microsoft.com/azure/sql-database/sql-database-read-scale-out?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Report across scaled-out data tier](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-query-horizontal-partitioning?WT.mc_id=pid:13491:sid:32630431/)<br>
* [Manage file space for single and pooled databases] (https://docs.microsoft.com/azure/sql-database/sql-database-file-space-management)
