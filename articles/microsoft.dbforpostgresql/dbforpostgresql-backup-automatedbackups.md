<properties
    pageTitle="Automated backups in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Automated backups"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32639968"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8d101db0-cc7c-4c31-a9da-3f85bf9c063d"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Automated backups

Azure Database for PostgreSQL automatically takes backups of your server. The backups are used to support the point-in-time and geo restore features. Users do not have direct access to the backups and cannot change the timing of when backups are taken. Generally, full backups occur weekly and differential backups occur twice a day for servers with a max supported storage of 4 TB. Snapshot backups happen at least once a day for servers that support up to 16 TB of storage. Transaction log backups in both cases occur every five minutes. The default retention period for backups is 7 days and can be increased to 35 days.

Azure Database for PostgreSQL provides up to 100% of your provisioned server storage size as backup storage at no additional cost. Typically, this corresponds to a backup retention of 7 days. You can track this storage with the metric Backup Storage Used.

You can choose to take a dump of a database on your server using [pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore).

## **Recommended Steps**

* Servers that can scale up to 16 TB do not yet have a backup storage metric available. Backups are being taken for these servers, as described above. Work is in progress to provide a backup storage metric.
* These backup files cannot be exported and can only be used for restores in-service. If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import) steps.
* Backup storage metric increasing unexpectedly: If you have an increased number of transactions in your database, the transaction log, and as a result its backups, also becomes larger. These backups are retained till they are past your selected retention days. 

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [How-to restore a PostgreSQL server using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)<br>
* [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
