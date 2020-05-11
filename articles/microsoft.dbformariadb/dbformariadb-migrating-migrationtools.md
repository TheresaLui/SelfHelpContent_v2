<properties
    pageTitle="Migration tools for Azure Database for MariaDB"
    description="Migration tools for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="270"
    selfHelpType="generic"
    supportTopicIds="32640132"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0aeed8a0-d32b-4f92-a363-7637e3b5694e"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Migration tools for Azure Database for MariaDB

There are many different ways a database server can be migrated. The best solution depends on many factors including: How much data needs to be moved, can downtime be tolerated, does your application move as well, where your current server is location (on-premises, in a virtual machine, in a different cloud), and more.

Most question around migration tools and recommendations can be solved by working through the recommended steps.

## **Recommended Steps**

* If you are migrating using dump & restore and encounter problems, familiarize yourself with [Migrate your MariaDB database to Azure Database for MariaDB using dump and restore](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore/) how-to

If you are using dump and restore:

* Make sure to use database dumps when you are migrating the entire databases
* If you encountered the "MySQL server has gone away" error, increase the value of the `max_allowed_packet` parameter to higher value (like *1234567899*) in portal, then add the `max_allowed_packet` parameter in your mysqldump command: 

    `$ mysqldump --max-allowed-packet=1234567899 -u root -p testdb > testdb_backup.sql`

* Make sure all tables in the database use the InnoDB storage engine when loading data into Azure Database for MariaDB
* To avoid any compatibility issues, ensure the same version of MariaDB is used on the source and destination systems when dumping databases

## **Recommended Documents**

* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb)<br>
* [Migrate MariaDB using dump and restore](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore/)
