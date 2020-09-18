<properties
    pageTitle="Setting up monitors and alerts"
    description="Setting up monitors and alerts"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="580"
    selfHelpType="generic"
    supportTopicIds="32640066"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7e84a69d-fc1b-4983-a234-66ba592665c1"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Setting up monitors and alerts

Azure Database for MySQL offers two deployment types - single server and flexible server. You can set up alert on metrics for your Azure database for MySQL.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you are having trouble creating and managing metric alerts, review the [set up alerts on metrics on flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/howto-alert-on-metric/) or [set up alerts on metrics on Single Server](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/) how-to.
* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az monitor metrics alert** with valid values. Review the [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) documentation for valid parameters.

* If you are having trouble using Azure Rest API:

  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse)
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

## **Recommended Documents**

* [Understand your Azure Database for MySQL Flexible Server resources using metrics](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-monitoring)
* [Create an alert rule on a Single Server metric from Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/howto-alert-on-metric/)
* [Create an alert rule on a Single Server metric from Azure portal](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/)
