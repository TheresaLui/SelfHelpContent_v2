<properties
    pageTitle="Issues with migrating to Azure Database for PostgreSQL"
    description="Outlines issues that customers might encounter during migration"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ankam"
    ms.author="ankam"
    displayOrder="310"
    selfHelpType="generic"
    supportTopicIds="32639991"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75c11e4e-5d20-48e4-ac05-0b88608d77ce"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with migrating to Azure Database for PostgreSQL

Migrating a database server can have many facets and the best method to use depends on many factors such as how much data needs to be moved, how much downtime can be tolerated, whether your application needs to move as well, and so on.

Most migration problems can be solved by working through the recommended steps.

## **Recommended Steps**

* If you are evaluating different migration options, consult our [Azure Database Migration Guide](https://datamigration.microsoft.com/)
* If you are migrating yourself (e.g. using dump and restore) and encounter problems, consider using the [Data Migration Service](https://azure.microsoft.com/services/database-migration/)
* If you are using the Data Migration Service and experience problems, work through the [step-by-step tutorials for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online)
  * Address issues with [online migration configuration](https://docs.microsoft.com/azure/dms/known-issues-azure-postgresql-online#online-migration-configuration)
  * Address [datatype limitations](https://docs.microsoft.com/azure/dms/known-issues-azure-postgresql-online#datatype-limitations)
  * Address [LOB limitations](https://docs.microsoft.com/azure/dms/known-issues-azure-postgresql-online#lob-limitations)
  * Address [other common issues](https://docs.microsoft.com/azure/dms/known-issues-azure-postgresql-online#other-limitations)

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql)<br>
* [Azure Database Migration Guide](https://datamigration.microsoft.com/)<br>
* [Data Migration Service](https://azure.microsoft.com/services/database-migration/)
