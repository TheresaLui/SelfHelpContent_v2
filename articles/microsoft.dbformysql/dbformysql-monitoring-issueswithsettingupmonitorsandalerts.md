<properties
    pageTitle="Issues with setting up monitors and alerts"
    description="Issues with setting up monitors and alerts"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="260"
    selfHelpType="generic"
    supportTopicIds="32640066"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="254cd337-001c-4bd8-b997-6fef00412b75"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues with setting up monitors and alerts

In Azure Database for MySQL, you can alert on metrics for your Azure services.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you are having trouble creating and managing metric alerts using Azure portal, review the [Set up alerts on metrics](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal//) how-to
* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az monitor metrics alert** with valid values. Review the [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) documentation for valid parameters.

* If you are having trouble using Azure Rest API:

  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse)
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

## **Recommended Documents**

* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric#create-an-alert-rule-on-a-metric-from-the-azure-portal/)<br>
* [How to configure webhooks in alerts.](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks/)<br>
* [Overview of metrics collection](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform#metrics/)
