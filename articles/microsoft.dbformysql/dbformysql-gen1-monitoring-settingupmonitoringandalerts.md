<properties
  pagetitle="Setting up monitors and alerts&#xD;"
  description="Setting up monitors and alerts"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="ambhatna,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747587"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2595a05d-aa2e-446d-83ba-15b5e492c96f"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Setting up monitors and alerts

Azure Database for MySQL offers two deployment types: single server and flexible server. You can set up alerts on metrics for your Azure Database for MySQL implementation.

Most users can resolve their issues by considering the following points.

### Considerations

* If you're having trouble creating and managing metric alerts, review the topic [Set up alerts on metrics on flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric/) or [Set up alerts on metrics on Single Server](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/).
* If you're having trouble using the Azure CLI:

  * Make sure that you are signed-in to the correct account by using `az login`
  * Ensure you are using the correct subscription if you have multiple subscriptions.
  * Specify all required parameters in `az monitor metrics alert` using valid values. Review the topic [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) for valid parameters.

* If you are having trouble using the Azure Rest API:

  * Familiarize yourself with the [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse).
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

## **Recommended documents**

* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)
* [Create an alert rule on a Single Server metric from Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-alert-on-metric/)
* [Create an alert rule on a Single Server metric from Azure portal](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/)
