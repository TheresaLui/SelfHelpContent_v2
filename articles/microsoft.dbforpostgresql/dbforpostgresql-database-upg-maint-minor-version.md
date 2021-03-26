<properties
    pageTitle="Upgrades and Maintenance Azure Database for PostgreSQL"
    description="Guidance when upgrading/maintaining Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32788716, 32789538"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7c60337c-7b5a-4bbf-92d2-044db5e4f0e1"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
 
# PostgreSQL minor version upgrades

**Minor version upgrades**: minor version of the database is automatically upgraded as part of maintenance operations.

## **Recommended Steps**

* How do I find out which minor version of the PostgreSQL Engine I am running?
  <br> For single Server, review [Supported PostgreSQL Versions](https://docs.microsoft.com/azure/postgresql/concepts-supported-versions)

* How soon can I expect a minor version on boarded on Single Server after it has been released?
  <br>We target onboarding of the minor version within 3 months of its release. In some cases, we apply critical patches and security fixes from the latest versions.
  
* Will I incur a downtime when a new minor version is onboarded?
  <br>Yes, the minor version upgrade is folded into maintenance operation, which forces a restart.


## **Recommended Documents**
* [Planned maintenance in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification)
