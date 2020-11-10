<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32640083"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec, Mooncake"
    articleId="53cc541f-c3de-406e-93cf-cab3a0842fce"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. In-place restores and restoring individual databases within a server are not supported.

The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically and users do not have access to the backups. Because transaction log backups are taken every 5 minutes, you may need to wait 5 minutes before you're able to restore to a specific point-in-time within a 5 minute interval.

**NOTE**: **For Azure Database for MySQL Flexible servers, you can reduce the backup period to minimum 1 day.**

## **Recommended Steps**

* If you are having connectivity issues after restoring the server, make sure that the connection string is referring to the restored server and username has the servername of restored server in the `username@servername` for single server. In case of flexible server, you can simply use the `username` on the restored server.
* Ensure that you try to restore to a point in time that is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
* The point in time restore duration depends on your database size and the transaction log size from last full backup. The restore operation can take upto 12 hrs and is dependent on multiple factors including storage provisioned, ongoing transactions on the server etc.
* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)

## **Recommended Documents**

*   Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
*   Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
*   How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
*   How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
*   [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
