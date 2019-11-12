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
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="8d101db0-cc7c-4c31-a9da-3f85bf9c063d"
/>

# Automated backups

Azure Database for PostgreSQL automatically takes backups of your server. The backups are used to support the point-in-time and geo restore features. Users do not have direct access to the backups and cannot change the timing of when backups are taken. Generally, full backups occur weekly, differential backups occur twice a day, and transaction log backups occur every five minutes. The default retention period for backups is 7 days and can be increased to 35 days.

You can choose to take a dump of a database on your server using [pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore).

## **Recommended Steps**

* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [How-to restore a PostgreSQL server using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)<br>
* [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
