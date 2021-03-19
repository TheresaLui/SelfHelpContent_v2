<properties
    pageTitle="Planned Maintenance Azure Database for PostgreSQL"
    description="Planned maintenance Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32789534, 32788705"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b233662c-1750-4250-b156-f9c104db2540"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Planned maintenance in Azure Databases for PostgreSQL - Single Server

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region. During planned maintenance, a notification event is created to inform customers when the service update is deployed in the Azure region hosting their servers.

## **Recommended Steps**

* How can I receive advanced notification for scheduled maintenance?

  You can receive alerts for upcoming planned maintenance using:
  * Alerts: You can configure alerts for an upcoming planned maintenance event. Refer to [how can I get notified of planned maintenance](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification#how-can-i-get-notified-of-planned-maintenance) to configure alerts.
  * Azure portal: Refer to [planned maintenance notification from Azure portal](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification#check-planned-maintenance-notification-from-azure-portal) for more details.


* Can I change the day/time of the maintenance specified in the notification?

     No. After the notification is sent to a given Azure region, the patching schedule changes cannot be made for an individual server in that region. The patch is rolled out to all servers in the entire region in the same planned maintenance deployment process.

* How does Azure coordinate patching of different regions?

    Regions are not patched at the same time. Maintenance deployments are typically completed overnight to avoid work hours, typically 5 PM - 8 AM, although the exact start and end times can vary



## **Recommended Documents**

* [Planned maintenance notification in Azure Databases for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification)
