<properties
    pageTitle="Backups and restore options for Azure Database for MariaDB"
    description="Backups and restore options for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32640113"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="55c846e2-cd1a-4155-b3d2-dea2939ee727"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Backups and restore options for Azure Database for MariaDB

Azure Database for MariaDB automatically takes backups of your server. The backups are used to support our point-in-time restore feature. Users do not have access to the backups and cannot change the timing of when backups are taken. Generally, full backups occur weekly and differential backups occur twice a day for servers with a max supported storage of 4 TB. Snapshot backups happen at least once a day for servers that support up to 16 TB of storage. Transaction log backups in both cases occur every five minutes. The default retention period for backups is 7 days and can be increased to 35 days.

## **Recommended Steps**

* If you want to export the MariaDB database, review [How to export MariaDB database using PHPMyAdmin](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore#export-using-phpmyadmin)

## **Recommended Documents**

* [Azure Database for MariaDB business continuity overview](https://docs.microsoft.com/azure/mariadb/concepts-business-continuity)<br>
* [Azure Database for MariaDB backup and restore concepts](https://docs.microsoft.com/azure/mariadb/concepts-backup)<br>
* [How to restore a MariaDB server using the Azure portal](https://docs.microsoft.com/azure/mariadb/howto-restore-server-portal)<br>
* [How to restore a MariaDB server using the Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-restore-server-cli)
