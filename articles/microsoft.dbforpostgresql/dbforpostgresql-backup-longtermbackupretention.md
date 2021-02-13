<properties
    pageTitle="Long term retention of backups for Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Long term retention"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32639993, 32780982"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6d0360ff-6ed5-4f4b-8d0a-7f56129afb42"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Long term retention of backups

Long term retention of backup (longer than 35 days) is currently not natively integrated within the service. However you can choose from the below options.

1. [Azure Backup for PostgreSQL - Preview](https://docs.microsoft.com/en-us/azure/backup/backup-azure-database-postgresql).
2. You have the option to use *pg_dump* to take backups and store them for long term retention. 
3. Use third party solutions.

## **Recommended Steps**

* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [Migrate your PostgreSQL database using dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore)<br>
* [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
