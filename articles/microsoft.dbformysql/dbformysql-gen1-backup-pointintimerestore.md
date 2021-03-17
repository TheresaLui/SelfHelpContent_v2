<properties
  pagetitle="Backups and restore options for Azure Database for MySQL&#xD;"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="manishku,bahusse"
  selfhelptype="Generic"
  supporttopicids="32747575"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake"
  articleid="7fd438af-9966-4776-8dac-208e35f4859f"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Backups and restore options for Azure Database for MySQL

Resolve issues with backups and restore options using the following solutions.

## Common questions

* **Restore was successful, but still seeing current data in the restored server**<br>
Often, users report that their point in time restores show recent (current) data in the restored server. This occurs because of an incorrect connection string when connecting to the restores server. For details, review [this tutorial](https://techcommunity.microsoft.com/t5/azure-database-support-blog/point-in-time-restore-in-azure-database-for-mysql-and-azure/ba-p/772655).

* **Where are my backups?** <br>
Azure Database for MySQL automatically creates server backups and stores them in user-configured locally redundant or geo-redundant storage. Backups can only be used to restore your server to a point-in-time using the **Restore** button on the Overview pane on the Azure portal. See [Backup and restore in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-backup).

* **Backup failing using MySQL Workbench or taking a cold backup?**<br>
Review this document: [Export your Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/backup-azure-database-for-mysql-to-a-blob-storage/ba-p/803830).

* **Restore server beyond retention?**<br>
Ensure that you restore to a point in time that is within your configured retention period. Backups are not backfilled when you increase the retention period.

* **Database corrupted?** <br>
See [Troubleshoot database corruption in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/how-to-fix-corrupt-database).

* **User access issue for the restored server/ Access denied** <br>
   Read the following guides:<br>
   * [Azure MySQL migration best practices](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online).
   * [Export and import MySQL users and privileges to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/export-and-import-mysql-users-and-privileges-to-azure-database/ba-p/916995).
   * [Tips and Tricks in using mysqldump and mysql restore to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912).

* **Migrate MySQL to Azure Database for MySQL online?** <br>
   See this [Tutorial: Migrate MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#prerequisites).

* **Retention less than 7 days or beyond 35 days?** <br>
   The default retention period is 7 days and can be increased up to 35 days. In Azure MySQL single server, you can't set retention for less than 7 days or beyond 35 days. But you may [Automate backups of your Azure Database for MySQL server to azure storage for longer term retention](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/automate-backups-of-your-azure-database-for-mysql-server-to/ba-p/1791157). For Azure Database for MySQL Flexible servers, you can reduce the backup period to minimum 1 day.

* **Point in time restore to other subscriptions**

   Restore servers are always created in the same resource group and same subscription as the existing server. If you want to restore server in a different resource group or different subscription, you can [move the restore server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation. Also you can refer to [Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/restore-your-azure-database-for-mysql-server-into-a-different/ba-p/1043570) blog.

## **Recommended Steps**

* Azure Database for MySQL supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. In-place restores and restoring individual databases within a server are not supported.

* The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically and users do not have access to the backups. Because transaction log backups are taken every 5 minutes, you may need to wait 5 minutes before you're able to restore to a specific point-in-time within a 5 minute interval.

* If you are having connectivity issues after restoring the server, make sure that the connection string is referring to the restored server and the username has the servername of restored server in the `username@servername` for single server. In case of flexible server, you can simply use the `username` on the restored server.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
* The point in time restore duration depends on your database size and the transaction log size from last full backup. The restore operation can take up to 12 hrs and is dependent on multiple factors including storage provisioned, ongoing transactions on the server etc.
* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)

## **Recommended Documents**

* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity).
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore).
* How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal).
* How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli).
* [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli).
