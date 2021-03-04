<properties
    pageTitle="Backups and restore options for Azure Database for MySQL Flexible Server"
    description="Backups and restore options for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32747629"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec, Mooncake"
    articleId="819ba0f5-212c-438c-941c-225f4bcfa361"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible server supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. Additionally, the new server has the exact same configuration as that of the old server. In-place restores and restoring individual databases within a server are not supported.

The default retention period is 7 days and can be changed from any time to 1 to 35 days. The backups required to support this functionality are taken automatically and users do not have access to the backups. Because transaction log backups are taken every 5 minutes, you may need to wait 5 minutes before you're able to restore to a specific point-in-time within a 5 minute interval. Additionally, you can directly go to the **Latest Restore Point** by using the default point-in-time restore operation.

## **Recommended Steps**

* If you're having connectivity issues after restoring the server, make sure that the connection string is referring to the restored server and you're connecting to the server using the steps detailed here.
* Ensure that you try to restore to a point in time that is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* You can restore to the latest possible restored point for the server that is available by default.
* The point-in-time restore duration depends on your database size and the transaction log size from last full backup. The SLA of restore time is 12 hours.
* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)
* Restore servers are always created in the same resource group and same subscription as the existing server. If you want to restore server in a different resource group or different subscription, you can [move the restore server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation.

## **Recommended Documents**

*   [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
*   [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
*   [How to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
