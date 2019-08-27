<properties
    pageTitle="Migration Tools for MySQL"
    description="Outlines details about Database Migration Service"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jtoland"
    ms.author="jtoland,ankam"
    displayOrder="270"
    selfHelpType="generic"
    supportTopicIds="32640069"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="4acf8133-6c71-4ef1-a9dc-bc8310c40650"
/>

# Migration tools for Azure Database for MySQL

There are many different ways a database server can be migrated. The best solution depends on many factors including: How much data needs to be moved, can downtime be tolerated, does your application move as well, where your current server is location (on-premises, in a virtual machine, in a different cloud), and more.

Most question around migration tools and recommendations can be solved by working through the recommended steps.

## **Recommended Steps**

* Review the [Azure Database Migration Guide](https://datamigration.microsoft.com/)
* Review the [Migrate MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online) tutorial.
* If you are migrating using dump and restore, or data-in-replication and encounter problems, familiarize yourself with [Migrate your MySQL database to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/) how-to
* If you are using dump and restore
  * Make sure to use database dumps when you are migrating the entire databases.
  * Make sure all tables in the database use the InnoDB storage engine when loading data into Azure Database for MySQL.
  * To avoid any compatibility issues, ensure the same version of MySQL is used on the source and destination systems when dumping databases.

## **Recommended Documents**

* [Data Migration Service](https://azure.microsoft.com/services/database-migration/)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)<br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)<br>
* [Data-in Replication in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-data-in-replication/)<br>
* [Migrate MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)
