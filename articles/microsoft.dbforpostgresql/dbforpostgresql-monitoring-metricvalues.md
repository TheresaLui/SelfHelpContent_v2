<properties
    pageTitle="Issues with metrics shown in the portal"
    description="Issues with metrics shown in the portal"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="290"
    selfHelpType="generic"
    supportTopicIds="32639994, 32780885"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5db270cf-b172-4294-b797-e6611df93546"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with metrics shown in the portal

The metrics shown in Azure Database for PostgreSQL - Single server portal are numerical values that describe some aspect of a system at a particular **point in time**.

Most users are able to resolve their issue using the following steps.

## **Recommended steps**

* Does **storage metric** show more storage used than when you directly query the database?

  * Beyond the data actually stored in your database in the supporting indexes, the footprint of your server includes additional files such as the transaction log, and other files needed to run the managed server. As such, there is a difference in storage used if you are only querying for data stored and indexes.

* Does the metric show different values at different times?

    * Note that the metrics describe some aspect of a system at a particular point in time. For example, maximum number of active connection will differ when you check at different points of time.

* Are you trying to enable **Query Performance Insight**, Performance Recommendations, or Query Store on a replica server or on a server that was previously a replica?

   * Replicas do not support Query Performance Insight and Performance Recommendation features. The Query Store database on replicas is a copy of the primary server's Query Store data.
   
   * After a replica becomes a standalone server, [set **Query Store parameters**](https://docs.microsoft.com/azure/postgresql/concepts-query-store#enabling-query-store) and restart the former replica to activate the feature.

## **Recommended documents**

* [Interacting with Azure Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#interacting-with-azure-monitor-metrics/)<br>
* [Thinking through metrics](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/taking-postgres-s-temperature-with-these-4-system-metrics/ba-p/1187969)
* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/postgresql/howto-alert-on-metric/)
