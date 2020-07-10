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
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="62d59e94-5a7b-4819-81af-b664886c50bf"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Geo-redundant backups and geo-restore

Geo-restore backups can only be configured at the time an Azure Database for PostgreSQL server is created. If configured, the last known good backup is geo-redundantly stored and a new server can be created in a different Azure region. Geo-restore does not allow you to chose a point in time. Instead the restore is to the most recent geo-replicated backup, typically within the last hour. Restoring individual databases within a server is not supported.

## **Recommended Steps**

* If you try to restore a server in a different region and you are not seeing backups to restore from, make sure that the source server was created with geo-restore backups turned on
* If after you access the new server you see inconsistent data, confirm that the connection string (in particular the user field: username@servername) references the new server
* The new server created during a restore does not have the firewall rules or VNet service endpoints that existed on the original server. These rules need to be set up separately for this new server. If you receive a pg_hba error, it indicates that your client's IP has not been allowed for this server.
* Basic tier servers do not support geo-restore. 
* Review the [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity) to understand estimated restore times and restore point objectives
* Review the [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup) to understand supported functionality and regional coverage
* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)

## **Recommended Documents**

* [How-to restore a PostgreSQL server using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)
