<properties
    pageTitle="Upgrades and Maintenance Azure Database for PostgreSQL"
    description="Guidance when upgrading/maintaining Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32788715, 32789536"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7c60337c-7b5a-4bbf-92d2-044db5e4f0e1"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
 
# PostgreSQL minor version upgrades

**Minor version upgrades**: minor version of the database is automatically upgraded as part of maintenance operations.

## **Recommended Steps**
* How do I find what is the minor version of the PostgreSQL Engine I am running?

    For single Server you can find out the supported minor version [Supported PostgreSQL Versions](https://docs.microsoft.com/azure/postgresql/concepts-supported-versions)
* How soon can I expect a minor version on boarded on Single Server after it has been released?

    We typically target on boarding the minor version within 3 months of its release. In some cases, we do pick and apply critical patches and security fixes from the latest versions
* WIll I incur a downtime when a new minor version is on boarded
    
    Yes, the minor version upgrade is folded into maintenance operation which will force a restart.


## **Recommended Documents**
* [Planned maintenance in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification)
