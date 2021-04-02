<properties
  pagetitle="Setting up monitors and alerts&#xD;"
  description="Setting up monitors and alerts"
  service="microsoft.dbformysql"
  resource="flexibleservers"
  ms.author="ambhatna,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747639"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="ef64491e-26fe-4213-a382-f41597d98047"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Setting up monitors and alerts

In Azure Database for MySQL Flexible Server, you can alert on metrics for your Azure services.

Most users can to resolve their issues after considering the following points.

### Considerations

* If you're having trouble creating and managing metric alerts using the Azure portal, see [Set up alerts on metrics](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric/).
* If you're having trouble using the Azure CLI:

  * Make sure you are signed-in to the correct account by using `az login`.
  * Ensure you are using the correct subscription if you have multiple subscriptions.
  * Specify all required parameters in `az monitor metrics alert` using valid values. See [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) for valid parameters.

* If you're having trouble using Azure Rest API:

  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse).
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

## **Recommended documents**

* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric/)
* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)