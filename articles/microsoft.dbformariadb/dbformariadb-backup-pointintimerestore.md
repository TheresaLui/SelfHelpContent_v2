<properties
    pageTitle="Backups and restore options for Azure Database for MariaDB"
    description="Backups and restore options for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32640145"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="b6c2dae7-fade-4ab5-a4cb-d333f5554cf0"
/>

# Backups and restore options for Azure Database for MariaDB

Azure Database for MariaDB supports point-in-time restore to any point within the configured backup retention period for a server. The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically. Because transaction log backups are taking every 5 minutes, restore to a point in time within the last 5 minutes might only be available 5 minutes after the point in time you want to restore to.

## **Recommended Steps**

* If you are having connectivity issues after restoring the server, make sure that the connection string is referring to the restored server
* Azure that you try to restore to a point in time that is within you configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
* The point in time restore duration depends on your database size and the transaction log size from last full backup. The SLA of restore time is 12 hours.
* If you want to export the MariaDB database, review [How to export MariaDB database using PHPMyAdmin](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore#export-using-phpmyadmin)

## **Recommended Documents**

* [Azure Database for MariaDB business continuity overview](https://docs.microsoft.com/azure/mariadb/concepts-business-continuity)<br>
* [Azure Database for MariaDB backup and restore concepts](https://docs.microsoft.com/azure/mariadb/concepts-backup)<br>
* [How to restore a MariaDB server using the Azure portal](https://docs.microsoft.com/azure/mariadb/howto-restore-server-portal)<br>
* [How to restore a MariaDB server using the Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-restore-server-cli)
