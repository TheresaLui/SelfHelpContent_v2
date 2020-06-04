<properties
    pageTitle="Availability and Connectivity/Unavailability was reported in Resource Health"
    description="Availability and Connectivity/Unavailability was reported in Resource Health"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,happynicolle"
    ms.author="saltug,nicw"
    supportTopicIds="32635223"
    productPesIds="15818"
    displayOrder="1"
    selfHelpType="generic"
    resourceTags=""
    articleId="dw-availabilityandconnectivity-unavailabilitywasreportedinresourcehealth.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Unavailability was reported in Resource Health

## **Recommended Steps**

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of Unavailable means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of Degraded means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

* Check [Microsoft Azure Service Dashboard](https://azure.microsoft.com/status/) for any known issues
* Check [Resource Health](https://docs.microsoft.com/azure/service-health/resource-health-overview) blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.
* Check the identified [maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/viewing-maintenance-schedule) for your data warehouse

## **Recommended Documents**

* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)
* [View maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/viewing-maintenance-schedule)
* [Change maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/changing-maintenance-schedule)
