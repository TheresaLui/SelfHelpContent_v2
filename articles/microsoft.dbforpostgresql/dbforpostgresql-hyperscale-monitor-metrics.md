<properties
    pageTitle="Metrics in Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Metrics in Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource="serverGroups"
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-monitor-metrics.md"
    selfHelpType="resource"
    supportTopicIds="32639994"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Metrics

Metrics in Azure Database for PostgreSQL - Hyperscale (Citus) are provided per node. Metrics are not aggregated a cluster level. However, with Azure Monitor [you can view metrics for multiple nodes on one chart](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#create-views-with-multiple-metrics-and-charts). 

Query Store is not an available feature in Hyperscale (Citus). Consider using the pg_stat_statements extension. 

## **Recommended Documents**
* [Metrics available in Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-monitoring)