<properties
    pageTitle="Metrics shown in the portal"
    description="Metrics shown in the portal"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="570"
    selfHelpType="generic"
    supportTopicIds="32640063"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d10a6261-a218-4bab-b4ce-5004c774a2a9"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Metrics shown in the portal

Azure Database for MySQL offers two deployment types - single server and flexible server. The metrics shown in portal are numerical values that describe some aspect of a system at a particular **point in time**.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Storage metric shows more storage used than directly querying database:

  * Beyond the data actually stored in your database, the footprint of your server includes additional files such as the transaction log, server log files and other files needed to run the managed server. As such, there is a difference in storage used if you are only querying for data stored and indexes.

* Metric show different value at different time:

    * Please note that the metrics describe some aspect of a system at a particular point in time. For example, maximum number of active connection will differ when you check at different points of time.

* Unable to view query text in Query Performance Insights in Azure Database for MySQL Single Server 

    * You must have an Owner or Contributor role to view the text of the queries in Query Performance Insight. If you have a Reader role, you can view charts and tables but not query text.

## **Recommended Documents**

* [Interacting with Azure Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#interacting-with-azure-monitor-metrics/)
* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/howto-alert-on-metric)
* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)
* [Create an alert rule on a metric in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/)