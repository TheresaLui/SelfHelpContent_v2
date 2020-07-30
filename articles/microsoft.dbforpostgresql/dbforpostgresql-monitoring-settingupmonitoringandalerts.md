<properties
    pageTitle="Issues with setting up monitors and alerts"
    description="Issues with setting up monitors and alerts"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="280"
    selfHelpType="generic"
    supportTopicIds="32640022"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7983296e-b490-453f-9244-e50acd80e869"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with setting up monitors and alerts

In Azure Database for PostgreSQL, you can alert on metrics for your Azure services. If you use [Azure Monitor Logs for your Postgres logs](https://docs.microsoft.com/azure/postgresql/concepts-server-logs), you can [configure log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log). 

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* If you are having trouble creating and managing metric alerts using Azure portal, review the [Set up alerts on metrics](https://docs.microsoft.com/azure/postgresql/howto-alert-on-metric) how-to
* If you are having trouble using Azure CLI:
  * Make sure you are signed in to the correct account using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az monitor metrics alert** with valid values. Review the [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) documentation for valid parameters.

* If you are having trouble using Azure Rest API:
  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse)
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

* If you are having trouble configuring planned maintenance notification, review [how to receive planned maintenance notification](https://docs.microsoft.com/azure/postgresql/concepts-monitoring#to-receive-planned-maintenance-notification)

## **Recommended Documents**

* [List of Azure Database for PostgreSQL metrics](https://docs.microsoft.com/azure/postgresql/concepts-monitoring)<br>
* [Create an alert rule on a metric from Azure portal](https://docs.microsoft.com/azure/postgresql/howto-alert-on-metric/)<br>
* [How to configure webhooks in alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks/)<br>
* [Overview of metrics collection](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform#metrics/)
