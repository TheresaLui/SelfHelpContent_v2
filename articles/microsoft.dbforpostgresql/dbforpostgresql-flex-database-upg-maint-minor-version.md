<properties
    pageTitle="Upgrades minor Azure Database for PostgreSQL"
    description="Guidance when upgrading minor version of Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32789537"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2045046d-88f6-4064-a9b3-35dc4c30caa2"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
 
# PostgreSQL minor version upgrades

**Minor version upgrades**: minor version of the database is automatically upgraded as part of maintenance operations.

## **Recommended Steps**
* How do I find what is the minor version of the PostgreSQL Engine I am running?

    For Flexible Server you can find out the supported minor version [Supported PostgreSQL Versions](https://docs.microsoft.com/en-us/azure/postgresql/flexible-server/concepts-supported-versions)
* How soon can I expect a minor version on boarded on Single Server after it has been released?

    We typically target on boarding the minor version within 3 months of its release. In some cases, we do pick and apply critical patches and security fixes from the latest versions
* WIll I incur a downtime when a new minor version is on boarded
    
    Yes, the minor version upgrade is folded into maintenance operation which will force a restart.

## **Recommended Documents**
* [Manage scheduled maintenance settings for Azure Database for PostgreSQL – Flexible server](https://docs.microsoft.com/azure/postgresql/flexible-server/how-to-maintenance-portal)
