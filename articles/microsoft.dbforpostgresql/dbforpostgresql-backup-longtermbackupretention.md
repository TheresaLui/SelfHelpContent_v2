<properties
    pageTitle="Long term retention of backups for Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Long term retention"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32639993"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6d0360ff-6ed5-4f4b-8d0a-7f56129afb42"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Long term retention of backups

Long term retention of backups (longer than 35 days) are currently not natively supported by the service. You have the option to use *pg_dump* to take backups and store them for long term retention. Third party solutions are available.

Native support for long term retention backups is currently being worked on by the Azure engineering team.

## **Recommended Steps**

* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [Migrate your PostgreSQL database using dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore)<br>
* [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
