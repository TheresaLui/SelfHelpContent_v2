<properties
    pageTitle="Backups and restore options for Azure Database for MariaDB"
    description="Backups and restore options for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32640124"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a95cfd01-9320-4d00-89e6-c3cff5f55bfe"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Backups and restore options for Azure Database for MariaDB

Geo-redundant backups can be configured at the time an Azure Database for MariaDB server is created. If configured, the last known good backup is geo-redundantly store and a new server can be created in a different Azure region. Geo-restore does not allow you to chose a point in time, but rather always restores to the last known good state. Restoring individual databases within a server is not supported.

## **Recommended Steps**

* If you try to restore a server in a different region and you are not seeing backups to restore from, make sure that the source server was created with geo-redundant backups turned on
* Review the [Azure Database for MariaDB business continuity overview](https://docs.microsoft.com/azure/mariadb/concepts-business-continuity) to understand estimated restore times and restore point objectives
* Review the [Azure Database for MariaDB backup and restore concepts](https://docs.microsoft.com/azure/mariadb/concepts-backup) to understand supported functionality and regional coverage
* If you want to export the MariaDB database, review [How to export MariaDB database using PHPMyAdmin](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore#export-using-phpmyadmin)

## **Recommended Documents**

* [How to restore a MariaDB server using the Azure portal](https://docs.microsoft.com/azure/mariadb/howto-restore-server-portal)<br>
* [How to restore a MariaDB server using the Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-restore-server-cli)
