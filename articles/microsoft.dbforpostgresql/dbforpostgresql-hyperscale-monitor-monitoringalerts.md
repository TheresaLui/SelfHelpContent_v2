<properties
    pageTitle="Metrics in Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Metrics in Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource=""
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-monitor-metrics.md"
    selfHelpType="generic"
    supportTopicIds="32640022, 32639998"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Setting up monitoring and alerts

We recommend that you configure alerting on Azure Database for PostgreSQL - Hyperscale (Citus). In Azure, you can have alerts on both metrics and logs.

Query Store is not an available feature in Hyperscale (Citus). Consider using the pg_stat_statements extension. 

## **Recommended Documents**
* [Create metric alerts in Hyperscale](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-alert-on-metric)
* [Azure Monitor Alerts overview](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-overview)
* [Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)
* [Metrics available in Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-monitoring)