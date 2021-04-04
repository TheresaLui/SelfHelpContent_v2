<properties
    pageTitle="Planned Maintenance Azure Database for PostgreSQL"
    description="Planned maintenance Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32789539"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fe50f8eb-6640-4598-8fde-c30beaa797e3"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Planned scheduled maintenance in Azure Databases for PostgreSQL - Single Server

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region.

## **Recommended Steps**
* Will I incur downtime during planned scheduled maintenance?

    Yes. Planned maintenance will lead to a brief (60-120 seconds) unavailability of the database server, but can be longer if there is high transactional activity and/or long running transactions. We recommend that you minimize the transactional load on the server during scheduled maintenance.

* How long will planned maintenance run within a region?

    Planned maintenance for a given Azure region is typically expected to run 8 hrs (11pm to 7am). During this time, Azure Database for PostgreSQL single servers are restarted. Restarts are typically expected to complete in 60-120 seconds. 
* Can I choose a custom maintenance window?

    Yes, you can choose to have maintenance done on a day and time of your choosing. The maintenance duration is 1 hour.
* How often maintenance is done?

    Typically, the minimum duration between two planned maintenance is 30 days. You will receive a notification of the next maintenance window 5 days in advance.

* How does Azure coordinate patching of different regions?

    Regions are not patched at the same time. Maintenance deployments are completed overnight to avoid work hours (typically 11 PM - 7 AM), although the exact start and end times can vary.



## **Recommended Documents**

* [Manage scheduled maintenance settings for Azure Database for PostgreSQL – Flexible server](https://docs.microsoft.com/azure/postgresql/flexible-server/how-to-maintenance-portal)
* [Scheduled maintenance in Azure Database for PostgreSQL – Flexible server.](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-maintenance)
