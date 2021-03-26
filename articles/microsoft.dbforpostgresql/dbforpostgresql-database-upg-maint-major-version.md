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
    articleId="94e04ccb-5511-4399-94d7-45328df079f4"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
 
# PostgreSQL major version upgrades

**Major version upgrades**: For upgrading your databases, you can perform a PostgreSQL dump and restore operation, or use Database Migration Service (DMS) to migrate your databases to a higher version.

## **Recommended Steps**

For major version upgrades, see [dump and restore documentation](https://docs.microsoft.com/azure/postgresql/how-to-upgrade-using-dump-and-restore). This guide provides several methods and step-by-step guides to perform upgrades. 

## **Recommended Documents**

* [Upgrade using dump and restore](https://docs.microsoft.com/azure/postgresql/how-to-upgrade-using-dump-and-restore)
* [Migrate database with dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore)
* [Migrate database with dump and psql](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
* [Minimal downtime migration with DMS](https://docs.microsoft.com/azure/postgresql/howto-migrate-online)
* [Azure Database for PostgreSQL versioning policy](https://docs.microsoft.com/azure/postgresql/concepts-version-policy)
