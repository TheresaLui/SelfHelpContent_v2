<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32640083"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="53cc541f-c3de-406e-93cf-cab3a0842fce"
/>

# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. In place restores are not supported. The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically. Because transaction log backups are taking every 5 minutes, restore to a point in time within the last 5 minutes might only be available 5 minutes after the point in time you want to restore to.

## **Recommended Steps**

* If you are having connectivity issues after restoring the server, make sure that the connection string is referring to the restored server
* If you get the below error while restoring the server, please refer to [Tips and Tricks in using mysqldump and mysql restore to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Tips-and-Tricks-in-using-mysqldump-and-mysql-restore-to-Azure/ba-p/916912)

    * "Access denied; you need (at least one of) the SUPER privilege(s) for this operation", please refer to solution for issue 1.
    * "Got error 1 from storage engine Operation failed with exitcode 1", please refer to solution for issue 3.
    * "You do not have the SUPER privilege and binary logging is enabled (you *might* want to use the less safe log_bin_trust_function_creators variable)Operation failed with exitcode 1", please refer to solution for issue 2.
    * "Table storage engine for 'mytable' doesn't have this option Operation failed with exitcode 1", please refer to solution 4.
* In Azure Database for MySQL, you cannot modify the "mysql.user" table. If you want to export MySQL users and privileges, please refer to [Export and import MySQL users and privileges to Azure Database for MySQL] (https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Export-and-import-MySQL-users-and-privileges-to-Azure-Database/ba-p/916995)
* Ensure that you try to restore to a point in time that is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
* The point in time restore duration depends on your database size and the transaction log size from last full backup. The SLA of restore time is 12 hours.
* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)
* If you want to backup Azure Database for MySQL to a Blob storage, please refer to [Backup Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)<br>
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup)<br>
* [How to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal)
