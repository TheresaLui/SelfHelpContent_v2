<properties
    pageTitle="Issues with metrics shown in the portal"
    description="Issues with metrics shown in the portal"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="250"
    selfHelpType="generic"
    supportTopicIds="32640063"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="93e2a07c-0431-4c0e-80d8-7912a4691dc2"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues with metrics shown in the portal

The metrics shown in Azure Database for MySQL portal are numerical values that describe some aspect of a system at a particular **point in time**.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Storage metric shows more storage used than directly querying database:

  * Beyond the data actually stored in your database, the footprint of your server includes additional files such as the transaction log, server log files and other files needed to run the managed server. As such, there is a difference in storage used if you are only querying for data stored and indexes.

* Metric show different value at different time:

    * Please note that the metrics describe some aspect of a system at a particular point in time. For example, maximum number of active connection will differ when you check at different points of time.

## **Recommended Documents**

* [Interacting with Azure Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#interacting-with-azure-monitor-metrics/)<br>
* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/)
