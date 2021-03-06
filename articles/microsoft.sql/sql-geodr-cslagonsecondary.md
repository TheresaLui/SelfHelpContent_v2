<properties
	pageTitle="Geo Replication, Failover Groups and DB Copy/Lag on geo-secondary database"
	description="Geo Replication, Failover Groups and DB Copy/Lag on geo-secondary database"
	service="microsoft.sql"
	resource="servers"
	authors="subbuk,maboja-msft,VMMicrosoft"
	ms.author="subbuk,maboja,vimahadi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32731232"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="e8b0bd9d-dfb4-4dc2-b094-1e3d19faeb8b"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Lag on Geo Secondary

**Lag on Secondary**

* Replication lag on secondary can occur due to combination of a heavy write workload on the Primary and imbalance between the service objective of Geo-Primary and Geo-Secondary where  Geo-Secondary unable to keep up.

* If you have a Geo-DR relationship between a largely different SLOs of Primary vs secondary (e.g., Primary w/Standard - S9 and Secondary w/ S0). The log holdup by the redo lagging on the secondaries instead of active transaction. For e.g., in Premium database, it has multiple replicas.  The logs generated by the primary are replicated to secondaries, and log are redone/replayed on the secondaries. Primary cannot truncate a log record until it has been redone on the all the secondaries. Azure SQL service has enabled parallel redo feature to speed up redo, and in most cases, the redo on the secondaries should be able to keep up with primary.  However, in certain cases, the redo work on the geo secondary side has be to serialized and this may cause redo lagging when the log generation rate on the primary is very high.

* To fix, Upgrading Geo-Secondary to the same service-objective as the Geo-Primary is recommended and should mitigate the issue on these scenarios.

## **Recommended Documents**

- [Configurable auto-failover groups](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group)
- [Scaling Databases](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale#dtu-based-purchasing-model-change-compute-resources-dtus)
- [Monitoring geo replication Lag](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication?WT.mc_id=pid:13491:sid:32731232/#monitoring-geo-replication-lag)<br>
