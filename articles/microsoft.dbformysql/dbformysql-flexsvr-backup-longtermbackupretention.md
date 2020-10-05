<properties
    pageTitle="Backups and restore options for Azure Database for MySQL Flexible Server"
    description="Backups and restore options for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="120"
    selfHelpType="generic"
    supportTopicIds="32747622"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="aa0cad28-b62c-4038-9c35-49ac7ee40902"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL Flexible Server

Long term retention backups are currently not natively supported by the service. You have the option to use **mysqldump** to take backups and store them for long term retention. Third party solutions are available.

Native support for long term retention backups is currently being worked on by the Azure engineering team.

## **Recommended Steps**

* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)
* If you want to backup Azure Database for MySQL to a Blob storage, please refer to [Backup Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)<br>
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup)
