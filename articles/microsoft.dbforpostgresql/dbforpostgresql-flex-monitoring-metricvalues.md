<properties
    pageTitle="Issues with metrics shown in the portal"
    description="Issues with metrics shown in the portal"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="290"
    selfHelpType="generic"
    supportTopicIds="32780880"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-monitoring-metricvalues"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with metrics shown in the portal

The metrics shown in Azure Database for PostgreSQL portal are numerical values that describe some aspect of a system at a particular **point in time**.

Most users are able to resolve issues using the steps below.

## **Recommended Steps**

* Storage metric shows more storage used than what you'll see by directly querying the database:

  * Beyond the data actually stored in your database in the supporting indexes, the footprint of your server includes additional files such as the transaction log, and other files needed to run the managed server. As such, there is a difference in storage used if you are only querying for data stored and indexes.

* Storage metric shows different values at different times:

    * Note that the metrics describe some aspect of a system at a particular point in time. For example, the maximum number of active connections will vary when you check at different points of time.


## **Recommended Documents**

* [Interacting with Azure Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#interacting-with-azure-monitor-metrics/)<br>
* [Thinking through metrics](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/taking-postgres-s-temperature-with-these-4-system-metrics/ba-p/1187969)
* [Create an alert rule on a metric](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)
