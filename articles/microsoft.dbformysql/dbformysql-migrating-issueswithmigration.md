<properties
    pageTitle="Issues with migrating to Azure Database for MySQL"
    description="Outlines issues that customers might encounter during migration"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jtoland"
    ms.author="jtoland,ankam"
    displayOrder="280"
    selfHelpType="generic"
    supportTopicIds="32640064"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f08de132-b511-4a81-a2f1-ecf5358f8a7a"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues with migrating to Azure Database for MySQL

Migrating a database server can have many facets and the best method to use depends on many factors such as how much data needs to be moved, can downtime be tolerated, does your application move as well, and so on.

Most migration problems can be solved by working through the recommended steps.

## **Recommended Steps**

* Make sure all tables in the database use the InnoDB storage engine when loading data into Azure Database for MySQL
* To avoid any compatibility issues, ensure the same version of MySQL is used on the source and destination systems when dumping databases
* In Azure Database for MySQL, you cannot modify the "mysql.user" table. If you want to export MySQL users and privileges, please refer to [Export and import MySQL users and privileges to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Export-and-import-MySQL-users-and-privileges-to-Azure-Database/ba-p/916995)
* If you get any of the below errors while restoring the server, please refer to [Tips and Tricks in using mysqldump and mysql restore to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Tips-and-Tricks-in-using-mysqldump-and-mysql-restore-to-Azure/ba-p/916912):

    * "Access denied; you need (at least one of) the SUPER privilege(s) for this operation", please refer to solution for issue 1
    * "Got error 1 from storage engine Operation failed with exitcode 1", please refer to solution for issue 3
    * "You do not have the SUPER privilege and binary logging is enabled (you *might* want to use the less safe *log_bin_trust_function_creators* variable) Operation failed with exitcode 1", please refer to solution for issue 2
    * "Table storage engine for 'mytable' doesn't have this option. Operation failed with exitcode 1", please refer to solution 4

* If you are migrating yourself (e.g. using dump and restore) and encounter problems, consider using the [Data Migration Service](https://azure.microsoft.com/services/database-migration/)
* If you are using the Data Migration Service and experience problems, work through the [step-by-step tutorials for Azure Database for MySQL](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)
* If you are migrating using the MySQL Workbench Database Migration Wizard, refer to the [MySQL Workbench](https://dev.mysql.com/doc/workbench/en/wb-migration.html) documentation

If you are using dump and restore:

* Make sure to use database dumps when you are migrating the entire databases
* If you encountered the "MySQL server has gone away" error, increase the value of the `max_allowed_packet` parameter to higher value (like *1234567899*) in portal, then add the `max_allowed_packet` parameter in your mysqldump command: 

    `$ mysqldump --max-allowed-packet=1234567899 -u root -p testdb > testdb_backup.sql`

## **Recommended Documents**

* [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql)<br>
* [Azure Database Migration Guide](https://datamigration.microsoft.com/)<br>
* [Data Migration Service](https://azure.microsoft.com/services/database-migration/)<br>
* [Migrate MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)<br>
* [Migrate using MySQL Workbench Database Migration Wizard](https://dev.mysql.com/doc/workbench/en/wb-migration.html)
