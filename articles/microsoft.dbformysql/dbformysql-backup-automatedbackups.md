<properties
  pagetitle="Backups and restore options for Azure Database for MySQL"
  description="Backups and restore options for Azure Database for MySQL"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="manishku,jtoland"
  selfhelptype="Generic"
  supporttopicids="32640046"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="01ba7d7f-1b5f-4f7d-9776-0319b9e4f3ea"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL automatically takes backups of your server, which are used to support our point-in-time restore feature. Users don't have access to these backups and cannot change backup timing. Generally, full backups occur weekly and differential backups occur twice a day for servers with a max supported storage of 4 TB. Snapshot backups happen at least once a day for servers that support up to 16 TB of storage. Transaction log backups in both cases occur every five minutes. The default backup retention period is 7 days, and this can be increased to 35 days or reduced to 1 day for the Azure Database for MySQL Flexible servers.

## **Recommended steps**

* See the topic [Import and export by using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench).
* To back up Azure Database for MySQL to a Blob storage, refer to the blog post [Back up Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

## **Recommended documents**

* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
* How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
* How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)