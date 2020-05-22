<properties
    pageTitle="Backups and restore options for Azure Database for MariaDB"
    description="Backups and restore options for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="120"
    selfHelpType="generic"
    supportTopicIds="32640131"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4cb93f8d-0bdd-4a78-a302-be1ff2530480"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Backups and restore options for Azure Database for MariaDB

Long term retention backups are currently not natively supported by the service. You have the option to use **mysqldump** to take backups and store them for long term retention. Third party solutions are available.

Native support for long term retention backups is currently being worked on by the Azure engineering team.

## **Recommended Steps**

* If you want to export the MariaDB database, review the [How-to export MariaDB database using PHPMyAdmin](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore#export-using-phpmyadmin)

## **Recommended Documents**

* [Azure Database for MariaDB business continuity overview](https://docs.microsoft.com/azure/mariadb/concepts-business-continuity)<br>
* [Azure Database for MariaDB backup and restore concepts](https://docs.microsoft.com/azure/mariadb/concepts-backup)
