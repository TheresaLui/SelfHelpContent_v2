<properties
  pagetitle="Metrics shown in the portal&#xD;"
  description="Metrics shown in the portal"
  service="microsoft.dbformysql"
  resource="flexibleservers"
  ms.author="ambhatna,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747624"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="e315b277-0f2c-4e06-bb05-901bb9a18eea"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Metrics shown in the portal

The metrics shown in Azure Database for MySQL Flexible Server portal are numerical values that describe some aspect of a system at a particular point in time.

Most users are able to resolve their issues after considering the following points.

### Considerations

* **Storage metric shows more storage used than when directly querying database.**

  Beyond the data actually stored in your database, the footprint of your server includes additional files such as the transaction log, server log files, and other files needed to run the managed server. As such, there is a difference in the storage used if you are only querying for data stored and indexes.

* **Metric shows a different value at different times.**

  Metrics describe some aspect of a system at a particular point in time. For example, the maximum number of active connection will differ when you check at different points in time.

## **Recommended documents**

* [Interacting with Azure Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#interacting-with-azure-monitor-metrics/)
* [Create an alert rule on a metric from the Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric)
* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)
