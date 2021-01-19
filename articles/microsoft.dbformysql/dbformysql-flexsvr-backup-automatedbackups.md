<properties
    pageTitle="Backups and restore options for Azure Database for MySQL Flexible Server"
    description="Backups and restore options for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32747600"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e920dc8b-22f6-42be-bedd-34abfb2591c2"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible automatically takes backups of your server. The backups are used to support our point-in-time restore feature. Users do not have access to the backups and cannot change the timing of when backups are taken. The first full snapshot backup is scheduled immediately after a server is created. This snapshot backup is retained as the server's base backup. Subsequent snapshot backups are differential backups only. Differential snapshot backups occur at least once a day. Differential snapshot backups do not occur on a fixed schedule. Differential snapshot backups occur every 24 hours unless the binary logs in MySQL exceeds 50-GB since the last differential backup. In a day, a maximum of six differential snapshots are allowed. Transaction log backups occur every five minutes.

The default retention period for backups is 7 days but can be changed to value between 1 to 35 days.

## **Recommended Steps**

* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)
* If you want to backup Azure Database for MySQL to a Blob storage, please refer to [Backup Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

## **Recommended Documents**

*   [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-servers/concepts-business-continuity)
*   [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/flexible-servers/concepts-backup-restore)
*   [How-to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/flexible-servers/how-to-restore-mysql-server-portal)
