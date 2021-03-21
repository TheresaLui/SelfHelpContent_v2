<properties
    pageTitle="Planned Maintenance notification Azure Database for PostgreSQL"
    description="Planned maintenance notification Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32789533"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9d54f43e-ce62-4257-a859-1a4cbc2cd05f"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Planned maintenance in Azure Databases for PostgreSQL - Single Server

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region. During planned maintenance, a notification event is created to inform customers when the service update is deployed in the Azure region hosting their servers.

## **Recommended Steps**
* Will I incur a downtime during planned scheduled maintenance?

    Yes. Planned maintenance will lead to a brief (60-120 seconds)unavailability of the database server but can be longer if there is high transactional activity and/or long running transactions. We recommend you minimize the transactional load on the server during scheduled maintenance

* How long planned maintenance run within a region?

    The default (system-managed) schedule is a random day of the week, and 60-minute window for maintenance start between 11pm and 7am local server time. If you want to customize this schedule, choose Custom schedule. You can then select a preferred day of the week, and a 60-minute window for maintenance start time

* How often maintenance is done?

    Typically, the minimum duration between two planned maintenance is 30 days. You receive a notification of the next maintenance window 5 days in advance

* How can I receive advanced notification for scheduled maintenance?

  You can receive alerts for upcoming planned maintenance using:
   * Email to a specific address
   * Email to an Azure Resource Manager Role 
   * Text message (SMS) to mobile devices
   * Pushed as a notification to an Azure app
   * Delivered as a voice message

* Can I change the day/time of the maintenance specified in the notification?

     No. After the notification is sent to a given Azure region, the patching schedule changes cannot be made for an individual server in that region. The patch is rolled out to all servers in the entire region in the same planned maintenance deployment process.

* How does Azure coordinate patching of different regions?

    Regions are not patched at the same time. Maintenance deployments are typically completed overnight to avoid work hours, typically 11 PM - 7 AM, although the exact start and end times can vary



## **Recommended Documents**

* [Manage scheduled maintenance settings for Azure Database for PostgreSQL – Flexible server](https://docs.microsoft.com/azure/postgresql/flexible-server/how-to-maintenance-portal)

