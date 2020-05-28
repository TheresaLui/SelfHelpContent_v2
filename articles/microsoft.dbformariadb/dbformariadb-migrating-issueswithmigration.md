<properties
    pageTitle="Issues with migrating to Azure Database for MariaDB"
    description="Issues with migrating to Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="280"
    selfHelpType="generic"
    supportTopicIds="32640129"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="908ab7e3-3ed4-49eb-bb0c-52f2900c61d2"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Issues with migrating to Azure Database for MariaDB

Migrating a database server can have many facets and the best method to use depends on many factors such as how much data needs to be moved, can downtime be tolerated, does your application move as well, and so on.

Most migration problems can be solved by working through the recommended steps.

## **Recommended Steps**

* If you are migrating using dump & restore and encounter problems, familiarize yourself with [Migrate your MariaDB database to Azure Database for MariaDb using dump and restore](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore/) how-to

If you are using dump and restore:

* Make sure to use database dumps when you are migrating the entire databases
* If you encountered the "MySQL server has gone away" error, increase the value of the `max_allowed_packet` parameter to higher value (like *1234567899*) in portal, then add the `max_allowed_packet` parameter in your mysqldump command: 

    `$ mysqldump --max-allowed-packet=1234567899 -u root -p testdb > testdb_backup.sql`

* Make sure all tables in the database use the InnoDB storage engine when loading data into Azure Database for MariaDB
* To avoid any compatibility issues, ensure the same version of MariaDB is used on the source and destination systems when dumping databases

## **Recommended Documents**

* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb)<br>
* [Migrate MariaDB using dump and restore](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore/)
