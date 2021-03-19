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

For long term backup retention of backups, you have following options:

* You can write a script to use mysqldump to backup your databases, and copy the dumpfile to Azure blob storage and automate to run it weekly, monthly or yearly based on your archival strategy. Our team has blogged a [step by step article](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/automate-backups-of-your-azure-database-for-mysql-server-to/ba-p/1791157) to achieve it.
* If you want to export the MariaDB database, review the [How-to export MariaDB database using PHPMyAdmin](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore#export-using-phpmyadmin)

## **Recommended Documents**

* [Azure Database for MariaDB business continuity overview](https://docs.microsoft.com/azure/mariadb/concepts-business-continuity)<br>
* [Azure Database for MariaDB backup and restore concepts](https://docs.microsoft.com/azure/mariadb/concepts-backup)
