<properties
    pageTitle="Setting up monitors and alerts"
    description="Setting up monitors and alerts"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="210"
    selfHelpType="generic"
    supportTopicIds="32747639"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ef64491e-26fe-4213-a382-f41597d98047"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Setting up monitors and alerts

In Azure Database for MySQL Flexible Server, you can alert on metrics for your Azure services.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you are having trouble creating and managing metric alerts using Azure portal, review the [Set up alerts on metrics](https://docs.microsoft.com/azure/mysql/flexible-server/howto-alert-on-metric/) how-to
* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az monitor metrics alert** with valid values. Review the [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) documentation for valid parameters.

* If you are having trouble using Azure Rest API:

  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse)
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

## **Recommended Documents**

* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/howto-alert-on-metric/)<br>
* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)