<properties
    pageTitle="Point-in-time restore in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL:point-in-time restore"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32640011"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7a6c959f-0671-48c4-9435-8051e7298f9d"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Point-in-time restore

Azure Database for PostgreSQL supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. In-place restores and restoring individual databases within a server are not supported.

The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically. Because transaction log backups are taken every 5 minutes, you may need to wait 5 minutes before you're able to restore to a specific point-in-time within a 5 minute interval.

## **Recommended Steps**

* If after you access the new server you see inconsistent data, confirm that the connection string (in particular the user field: username@servername) references the new server
* The new server created during a restore does not have the firewall rules or VNet service endpoints that existed on the original server. These rules need to be set up separately for this new server. If you receive a pg_hba error, it indicates that your client's IP has not been allowed for this server.
* Ensure that you try to restore to a point in time that is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)


## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [How-to restore a PostgreSQL server using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)<br>
* [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
