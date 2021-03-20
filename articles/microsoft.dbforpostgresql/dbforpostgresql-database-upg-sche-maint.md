<properties
    pageTitle="Planned Maintenance Azure Database for PostgreSQL"
    description="Planned maintenance Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32789540, 32788717"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b233662c-1750-4250-b156-f9c104db2540"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Planned scheduled maintenance in Azure Databases for PostgreSQL - Single Server

A planned maintenance is a maintenance window when service updates are deployed to servers in a given Azure region.

## **Recommended Steps**
* Will I incur a downtime during planned scheduled maintenance?

    Yes. Planned maintenance will lead to a brief (60-120 seconds)unavailability of the database server but can be longer if there is high transactional activity and/or long running transactions. We recommend you minimize the transactional load on the server during scheduled maintenance

* How long planned maintenance run within a region?

    Planned maintenance for a given Azure region is typically expected to run 15 hrs. During this time, Azure Database for PostgreSQL single servers are restarted and restarts are typically expected to complete in 60-120 seconds

* How often maintenance is done?

    Typically, the minimum duration between two planned maintenance is 30 days. You receive a notification of the next maintenance window 72 hours in advance


* How does Azure coordinate patching of different regions?

    Regions are not patched at the same time. Maintenance deployments are typically completed overnight to avoid work hours, typically 5 PM - 8 AM, although the exact start and end times can vary



## **Recommended Documents**

* [Planned maintenance in Azure Databases for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification)
