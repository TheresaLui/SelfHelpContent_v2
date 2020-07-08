<properties
    pageTitle="Metrics in Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Metrics in Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource="serverGroups"
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-monitor-metrics.md"
    selfHelpType="resource"
    supportTopicIds="32640022"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Setting up monitoring and alerts

We recommend that you configure alerting on Azure Database for PostgreSQL - Hyperscale (Citus). In Azure, you can have alerts on both metrics and logs.

Query Store is not an available feature in Hyperscale (Citus). Consider using the pg_stat_statements extension. 

## **Recommended Documents**
* [Create alerts in Hyperscale](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-alert-on-metric)
* [Azure Monitor Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-overview)