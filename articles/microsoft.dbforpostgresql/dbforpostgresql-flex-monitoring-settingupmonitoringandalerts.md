<properties
    pageTitle="Issues with setting up monitors and alerts"
    description="Issues with setting up monitors and alerts"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="280"
    selfHelpType="generic"
    supportTopicIds="32780883"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-monitoring-settingupmonitoringandalerts"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with setting up monitors and alerts

In Azure Database for PostgreSQL, you can alert on metrics for your Azure services. You can also [configure log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log). 


## **Recommended Steps**

* If you are having trouble creating and managing metric alerts, review the [Azure metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric) guide
* If you are having trouble using Azure CLI:
  * Ensure you are signed in to the correct account using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az monitor metrics alert** with valid values. Review the [Azure CLI Monitor Metrics](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli) documentation for valid parameters.

* If you are having trouble using Azure Rest API:
  * Familiarize yourself with [Components of a REST API request/response](https://docs.microsoft.com/rest/api/azure/#components-of-a-rest-api-requestresponse)
  * If your **Metric Alerts** deployment is failing, make sure required parameters are set and valid. See the [Metric alerts REST API documentation](https://docs.microsoft.com/rest/api/monitor/metricalerts).

