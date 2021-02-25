<properties
  pagetitle="Backups and restore options for Azure Database for MySQL"
  description="Backups and restore options for Azure Database for MySQL"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse,jtoland"
  selfhelptype="Generic"
  supporttopicids="32640046"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="01ba7d7f-1b5f-4f7d-9776-0319b9e4f3ea"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Automated backup for Azure Database for MySQL

**Where are my backups?** 

Azure Database for MySQL automatically creates server backups and stores them in user-configured, locally redundant storage or geo-redundant storage. You can use backups to restore your server to a point-in-time only by using the **Restore** button on the overview pane on Azure portal. See [Backup and restore in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-backup).

**Retention less than 7 days or beyond 35 days?** 

The default retention period is 7 days and can be increased up to 35 days. In Azure MySQL single server, you can't set retention for less than 7 days or beyond 35 days. But you can automate backups of your Azure Database for MySQL Server to Azure Storage (see **Recommended documents**). For Azure Database for MySQL Flexible servers, you can reduce the backup period to a minimum of 1 day.

**Azure Database for MySQL automatically takes backups of your server**

These backups are used to support our point-in-time restore feature. Users don't have access to these backups and cannot change backup timing. Generally, full backups occur weekly and differential backups occur twice a day for servers with a maximum supported storage of 4 TB. Snapshot backups happen at least once a day for servers that support up to 16 TB of storage. Transaction log backups in both cases occur every five minutes. The default backup retention period is 7 days. This period can be increased to 35 days or reduced to 1 day for the Azure Database for MySQL Flexible servers.

See the following considerations to resolve additional issues.

### Considerations

* To learn more about using MySQL Workbench, see [Import and export by using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench).
* To back up Azure Database for MySQL to a Blob storage, see [Back up Azure Database for MySQL to a Blob storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830).

## **Recommended documents**

* [Automate backups of your Azure Database for MySQL server to Azure Storage](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/automate-backups-of-your-azure-database-for-mysql-server-to/ba-p/1791157)**
* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
* How to restore a MySQL server using the Azure portal for [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
* How to restore a MySQL server using the Azure CLI for [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
