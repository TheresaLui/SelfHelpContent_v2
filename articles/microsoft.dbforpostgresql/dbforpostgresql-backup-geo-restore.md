<properties
    pageTitle="Geo-redundant backups and geo-restore in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Geo-redundant backups and geo-restore"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32639984"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="62d59e94-5a7b-4819-81af-b664886c50bf"
/>

# Geo-redundant backups and geo-restore

Geo-restore backups can only be configured at the time an Azure Database for PostgreSQL server is created. If configured, the last known good backup is geo-redundantly stored and a new server can be created in a different Azure region. Geo-restore does not allow you to chose a point in time, but rather always restores to the last known good state. Restoring individual databases within a server is not supported.

## **Recommended Steps**

* If you try to restore a server in a different region and you are not seeing backups to restore from, make sure that the source server was created with geo-restore backups turned on
* Review the [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity) to understand estimated restore times and restore point objectives
* Review the [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup) to understand supported functionality and regional coverage
* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)

## **Recommended Documents**

* [How-to restore a PostgreSQL server using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)
