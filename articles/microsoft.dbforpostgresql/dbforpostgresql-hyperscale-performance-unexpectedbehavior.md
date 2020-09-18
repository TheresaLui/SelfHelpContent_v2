<properties
    pageTitle="Unexpected behavior on Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Unexpected behavior on Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource="serverGroups"
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-performance-unexpectedbehavior.md"
    selfHelpType="resource"
    supportTopicIds="32640026, 32731228"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshoot unexpected behavior

## **Recommended Steps**
* If you recently added a new worker node, [make sure you rebalance the shards across nodes](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-scaling#rebalance-shards)
* Closing and opening connections frequently, especially when you have a high number of connections, will increase CPU and memory usage. Consider using long-lived connections and connection pooling. 
* Review [Azure Monitor metrics for your nodes](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-monitoring) for a high count of open connections. Query [pg_stat_activity](https://www.postgresql.org/docs/current/monitoring-stats.html#PG-STAT-ACTIVITY-VIEW) with `SELECT * FROM pg_stat_activity;` for more detail on which open connections are actively in use and which are open but idle. Each open connection holds on to cluster resources.
* Ingested data passes through the coordinator node. During ingestion, your coordinator may be bottlenecked. Consider [scaling up the coordinator node](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-scaling#increase-or-decrease-vcores-on-nodes) if this bottleneck occurs frequently.
