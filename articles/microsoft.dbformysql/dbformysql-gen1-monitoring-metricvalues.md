<properties
  pagetitle="Metrics shown in the portal&#xD;"
  description="Metrics shown in the portal"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="ambhatna,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747570"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="e74fbc06-3c4f-4d21-883a-3fc1d321e8b5"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Metrics shown in the portal

Azure Database for MySQL offers two deployment types: single server and flexible server. The metrics shown in portal are numerical values that describe some aspect of a system at a particular point in time.

Most users can resolve issues after considering the following points.

### Considerations

* **Storage metric shows more storage used than directly querying database.**

  Beyond the data actually stored in your database, the footprint of your server includes additional files such as the transaction log, server log files and other files needed to run the managed server. As such, there is a difference in storage used if you are only querying for data stored and indexes.

* **Metric shows a different value at a different time.**

  Metrics describe some aspect of a system at a particular point in time. For example, maximum number of active connections differs when you check at different points in time.

* **Unable to view query text in Query Performance Insights in Azure Database for MySQL Single Server.** 

  You must have an Owner or Contributor role to view the text of the queries in Query Performance Insight. If you have a Reader role, you can view charts and tables, but not query text.

## **Recommended documents**

* [Interacting with Azure Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#interacting-with-azure-monitor-metrics/)
* [Create an alert rule on a metric from the Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric)
* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)
* [Create an alert rule on a metric in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/)