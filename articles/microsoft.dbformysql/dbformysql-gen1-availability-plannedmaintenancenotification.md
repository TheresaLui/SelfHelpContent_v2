<properties
    pageTitle="Planned maintenance notification in Azure Databases for MySQL - Single Server"
    description="Planned maintenance notification in Azure Databases for MySQL - Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="700"
    selfHelpType="generic"
    supportTopicIds="32781079"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5fc0c889-1116-4153-80b6-bc01f257be47"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Planned maintenance notification in Azure Databases for MySQL - Single Server

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region. During planned maintenance, a notification event is created to inform customers when the service update is deployed in the Azure region hosting their servers

## **Recommended Steps**

* Once the notification is sent to a given Azure region, the patching schedule changes cannot be made for any individual server in that region. The patch is rolled out for entire region at once.
* All the Azure regions are patched during the deployment wise window timings and are not patched at the same time. The deployment wise window generally stretches from 5 PM - 8 AM local time next day, in a given Azure region.
* You can receive alert for upcoming planned maintenance using:

  * Using alerts: You can configure alerts for an upcoming planned maintenance event. Refer to [how can I get notified of planned maintenance](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification#how-can-i-get-notified-of-planned-maintenance) to configure alerts.
  * Azure portal: Refer to [planned maintenance notification from Azure portal](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification#check-planned-maintenance-notification-from-azure-portal) for more details.

* Minimum duration between two planned maintenance is 30 days. You receive a notification of the next maintenance window 72 hours in advance
* A planned maintenance for a given Azure region is typically expected to run 15 hrs. Azure Database for MySQL single servers are running in containers so database server restarts are typically quick, expected to complete typically in 60-120 seconds.

## **Recommended Documents**

* [Planned maintenance notification in Azure Databases for MySQL - Single Server](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification)
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
