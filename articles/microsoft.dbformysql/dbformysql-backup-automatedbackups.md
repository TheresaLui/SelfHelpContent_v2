<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32640046"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="01ba7d7f-1b5f-4f7d-9776-0319b9e4f3ea"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL automatically takes backups of your server. The backups are used to support our point-in-time restore feature. Users do not have access to the backups and cannot change the timing of when backups are taken. Generally, full backups occur weekly and differential backups occur twice a day for servers with a max supported storage of 4 TB. Snapshot backups happen at least once a day for servers that support up to 16 TB of storage. Transaction log backups in both cases occur every five minutes. The default retention period for backups is 7 days and can be increased to 35 days.

## **Recommended Steps**

* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)
* If you want to backup Azure Database for MySQL to a Blob storage, please refer to [Backup Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)<br>
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup)<br>
* [How-to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal)<br>
* [How-to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
