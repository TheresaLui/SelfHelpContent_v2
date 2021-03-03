<properties
    pageTitle="Point-in-time restore in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL:point-in-time restore"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32640011, 32780984"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7a6c959f-0671-48c4-9435-8051e7298f9d"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Point-in-time restore

Most users can find answers to questions and common issues by using the following information.

## Frequently asked questions

* **What is point-in-time recovery?** <br>
 Azure Database for PostgreSQL supports restoring to any point within the configured backup retention period for a server. 

* **Will the restore overwrite my server?** <br>
 No. The restore operation will create a new server side-by-side with the old server. In-place restores and restoring individual databases within a server are not supported. Also, only the backups performed by Azure Database for PostgreSQL can be restored.  

* **How far I can go back to restore?** <br>
 This depends on your retention period. The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically. 

* **What is the latest data I can restore to?** <br>
 In many cases, you will be able to restore within 5 minutes of the latest time. In other words, your data loss exposure is typically up to 5 minutes. Note that the time to recover depends on the size of data to restore from the backup, and the number of WAL files to recover to the time requested. 

* **Can I run multiple restores for the same server concurrently?** <br>
   We recommend you perform the restores sequentially, one after the other, for the same server.

* **Why I am not able to connect to my restored server?** <br>
  It's possible that you didn't change your server end point and/or the user name to `username@new-restored-server-name` in your connection string.

## **Recommended Steps**

* If, after you access the new server, you see inconsistent data, confirm that the connection string (in particular, the user field: `username@servername`) references the new server
* The new server created during a restore does not have the firewall rules or VNet service endpoints that existed on the original server. These rules need to be set up separately for this new server. If you receive a pg_hba error, it indicates that your client's IP is not allowed for this server.
* Ensure that you try to restore to a point in time that is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)


## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [How-to restore a PostgreSQL server using Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)<br>
* [How-to export PostgreSQL database using `pg_dump`](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
