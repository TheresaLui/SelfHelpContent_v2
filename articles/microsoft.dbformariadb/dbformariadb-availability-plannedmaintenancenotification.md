<properties
    pageTitle="Planned maintenance notification in Azure Databases for MariaDB"
    description="Planned maintenance notification in Azure Databases for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="700"
    selfHelpType="generic"
    supportTopicIds="32781078"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="bd7de921-29fc-43bf-984a-ef69b9638c19"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Planned maintenance notification in Azure Databases for MariaDB

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region. During planned maintenance, a notification event is created to inform customers when the service update is deployed in the Azure region hosting their servers.

## **Recommended Steps**

* After the notification is sent to a given Azure region, patching schedule changes cannot be made for an individual server in that region. The patch is rolled out to all servers in the entire region in the same planned maintenance deployment process.
* Regions are not patched at the same time. Maintenance deployments are typically completed overnight to avoid work hours, typically 5 PM - 8 AM, although the exact start and end times can vary.
* You can receive alerts for upcoming planned maintenance by using:

  * Alerts: Configure alerts for an upcoming planned maintenance event. See [how can I get notified about planned maintenance](https://docs.microsoft.com/azure/mariadb/concepts-planned-maintenance-notification#how-can-i-get-notified-of-planned-maintenance)?
  * Azure Portal: See [planned maintenance notification from Azure portal](https://docs.microsoft.com/azure/mariadb/concepts-planned-maintenance-notification#check-planned-maintenance-notification-from-azure-portal).

* Typically, the minimum duration between two planned maintenance windows is 30 days. You receive a notification of the next maintenance window 72 hours in advance.
* Planned maintenance for a given Azure region is typically expected to run 15 hrs. During this time, Azure Database for MariaDB servers are restarted. Restarts are expected to complete in 60-120 seconds.

## **Recommended Documents**

* [Planned maintenance notification in Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-planned-maintenance-notification)
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
