<properties
    pageTitle="Planned maintenance notification in Azure Databases for PostgreSQL - Single Server"
    description="Planned maintenance notification in Azure Databases for PostgreSQL - Single Server"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="700"
    selfHelpType="generic"
    supportTopicIds="32780766"
    resourceTags="servers, databases"
    productPesIds="17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="04ca8735-d0a3-4111-a870-d93e2ec4cdce"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Planned maintenance notification in Azure Databases for PostgreSQL - Single Server

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region. During planned maintenance, a notification event is created to inform customers when the service update is deployed in the Azure region hosting their servers

## **Recommended Steps**

* Once the notification is sent to a given Azure region, the patching schedule changes cannot be made for any individual server in that region. The patch is rolled out for entire region at once.
* All the Azure regions are patched during the deployment wise window timings and are not patched at the same time. The deployment wise window generally stretches from 5 PM - 8 AM local time next day, in a given Azure region.
* You can receive alert for upcoming planned maintenance using:

  * Using alerts: You can configure alerts for an upcoming planned maintenance event. Refer to [how can I get notified of planned maintenance](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification#how-can-i-get-notified-of-planned-maintenance) to configure alerts.
  * Azure portal: Refer to [planned maintenance notification from Azure portal](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification#check-planned-maintenance-notification-from-azure-portal) for more details.

* Minimum duration between two planned maintenance is 30 days. You receive a notification of the next maintenance window 72 hours in advance
* A planned maintenance for a given Azure region is typically expected to run 15 hrs. Azure Database for PostgreSQL single servers are running in containers so database server restarts are typically quick, expected to complete typically in 60-120 seconds.

## **Recommended Documents**

* [Planned maintenance notification in Azure Databases for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification)
