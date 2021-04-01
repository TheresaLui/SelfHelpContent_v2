<properties
  pagetitle="Backups and restore options for Azure Database for MySQL"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="manishku,bahusse,jtoland"
  selfhelptype="Generic"
  supporttopicids="32640083"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake"
  articleid="53cc541f-c3de-406e-93cf-cab3a0842fce"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Backups and restore options for Azure Database for MySQL

Resolve your issue by reviewing the following questions and solutions.

## Fix it yourself

* **Restore was successful, but still seeing current data in the restored server**<br>
   Often, users report that point-in-time restores show recent (current) data in the restored server. This occurs because of an incorrect connection string while connecting to the restored server. For details, review [this blog post](https://techcommunity.microsoft.com/t5/azure-database-support-blog/point-in-time-restore-in-azure-database-for-mysql-and-azure/ba-p/772655).

* **Can't find server backups**<br>
   Azure Database for MySQL automatically creates server backups and stores them in user-configured, locally redundant or geo-redundant storage. Backups can only be used to restore your server to a point-in-time. To do this, select the **Restore** button on the **Overview** pane in the Azure portal. See [Backup and restore in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-backup).

* **Backup fails using MySQL Workbench**<br>
   Try [Exporting your Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/backup-azure-database-for-mysql-to-a-blob-storage/ba-p/803830).

* **Restore server beyond retention**<br>
   Ensure that you restore to a point-in-time that is within your configured retention period. Backups are not backfilled after you increase the retention period.

* **Database is corrupted**<br>
   [Troubleshoot database corruption in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/how-to-fix-corrupt-database)

* **User access denied for the restored server** <br>
   Read the following guides:<br>
  * [Azure MySQL migration best practices](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online).
  * [Export and import MySQL users and privileges to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/export-and-import-mysql-users-and-privileges-to-azure-database/ba-p/916995).
  * [Tips and Tricks in using `mysqldump` and `mysql restore` to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912).

* **Error 1227 "Access denied; you need (at least one of) the SUPER privilege(s) for this operation"**<br>
  This error occurs after importing a dump file that contains definers. While Azure Database for MySQL is a managed PaaS solution and SUPER privileges are restricted, you can enable [log_bin_trust_function_creators](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) so that you can create definers without issue.

  For more information, see [ERROR 1227 (42000) at line 101: Access denied; you need (at least one of) the SUPER privilege(s) for this operation. Operation failed with exitcode 1](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1227-42000-at-line-101-access-denied-you-need-at-least-one-of-the-super-privileges-for-this-operation-operation-failed-with-exitcode-1).

* **Migrate MySQL to Azure Database for MySQL online**<br>
   Review [Tutorial: Migrate MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online#prerequisites).

* **Retention less than 7 or more than 35 days**<br>
   The default retention period is 7 days and can be increased up to 35 days. In Azure MySQL single server, you can't set retention less than 7 days or beyond 35 days. But you may [Automate backups of your Azure Database for MySQL server to azure storage for longer term retention](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/automate-backups-of-your-azure-database-for-mysql-server-to/ba-p/1791157). For Azure Database for MySQL Flexible servers, you can reduce the backup period to minimum 1 day.

* **Point-in-time restore to other subscriptions**<br>
   Restore servers are always created in the same resource group and same subscription as the existing server. If you want to restore a server in a different resource group or different subscription, you can [move the restore server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation. Also you can refer to [Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/restore-your-azure-database-for-mysql-server-into-a-different/ba-p/1043570) blog.

## Considerations

* Azure Database for MySQL supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. In-place restores and restoring individual databases within a server are not supported.

* The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically and users do not have access to the backups. Because transaction log backups are taken every 5 minutes, you may need to wait 5 minutes before you're able to restore to a specific point-in-time within a 5 minute interval.

## Quick tips

* If you're having connectivity issues after restoring the server, make sure that the connection string refers to the restored server and that the username has the server name of the restored server in the `username@servername` format for single server. In case of flexible server, simply use the `username` on the restored server.

* If you're trying to restore to a point-in-time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again

* The point-in-time restore duration depends on your database size and the transaction log size from last full backup. The restore operation can take up to 12 hrs and is dependent on multiple factors including storage provisioned, ongoing transactions on the server, and so on.

* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)

## **Recommended documents**

* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
* How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
* How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
* [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
