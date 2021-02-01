<properties
    pageTitle="Migration Tools for PostgreSQL"
    description="Outlines details about Database Migration Service"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ankam"
    ms.author="ankam"
    displayOrder="300"
    selfHelpType="generic"
    supportTopicIds="32781002, 32781003"
    resourceTags="servers, databases"
    productPesIds="16222, 17067, 17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="887f10ae-022c-4d47-aa08-e8d26697f858"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Migration tools for Azure Database for PostgreSQL

You can use the Azure Database Migration Service to perform an online migration of PostgreSQL databases running on-premises, in a virtual machine, or on Amazon RDS or EC2 to [Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/). Online migrations cause minimal downtime to the application.

## **Recommended Steps**

* [Address migration prerequisites](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#prerequisites)
* [Migrate the schema](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#migrate-the-sample-schema) using the pgdump utility
* [Provision an instance](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#provisioning-an-instance-of-dms-using-the-cli) of the Azure Database Migration Service
* Create and run a migration project:
* [Monitor the migration](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#understanding-migration-task-status)
* [Perform migration cutover](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#cutover-migration-task)

## **Recommended Documents**

* [Migrate PostgreSQL to Azure Database for PostgreSQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online)
* Database Migration Guide: [Migrate PostgreSQL to Azure Database for PostgreSQL](https://datamigration.microsoft.com/scenario/postgresql-to-azurepostgresql)
