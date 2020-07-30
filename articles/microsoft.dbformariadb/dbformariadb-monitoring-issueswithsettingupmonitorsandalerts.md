<properties
    pageTitle="Issues with setting up monitors and alerts"
    description="Issues with setting up monitors and alerts"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="260"
    selfHelpType="generic"
    supportTopicIds="32640130"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6f0029a5-2086-461d-b0f6-dfd76741b844"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Issues with setting up monitors and alerts

In Azure Database for MariaDB, you can alert on metrics for your Azure services.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you are having trouble creating and managing metric alerts using Azure portal, review the [Set up alerts on metrics](https://docs.microsoft.com/azure/mariadb/howto-alert-metric) how-to
* If you are having trouble using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az monitor metrics alert** with valid values. Review the [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) documentation for valid parameters.

* If you are having trouble using Azure Rest API:

  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse)
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

* If you are having trouble configuring planned maintenance notification, review [how to receive planned maintenance notification](https://docs.microsoft.com/azure/mariadb/concepts-monitoring#to-receive-planned-maintenance-notification)

## **Recommended Documents**

* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/mariadb/howto-alert-metric/)<br>
* [How to configure webhooks in alerts.](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks/)<br>
* [Overview of metrics collection](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform#metrics/)
