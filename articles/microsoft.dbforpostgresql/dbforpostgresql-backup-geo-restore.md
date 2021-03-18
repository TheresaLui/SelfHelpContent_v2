<properties
    pageTitle="Geo-redundant backups and geo-restore in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Geo-redundant backups and geo-restore"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32639984, 32780981"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="62d59e94-5a7b-4819-81af-b664886c50bf"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Geo-redundant backups and restores

Most users can resolve issues concerning geo-backup and geo-restore by using the following information.

## Frequently asked questions

* **What is geo-redundant backup and where it is stored?** <br>
  Geo-redundant backup is useful for both disaster recovery and business continuity. In the event of a primary region failure, you can restore the data at the remote region of your choice.

* **Is geo-redundant backup supported with all compute tiers?** <br>
  Geo-redundant backup is not supported with the Basic compute tier.
  
* **Why I am not able to configure geo-redundant backup for my server?** <br>
 Geo-restore backups can only be configured at the time that an Azure Database for PostgreSQL server is created. These backups can't be configured post-create. If you've created with local redundant backup and want to change to geo-backup, you need to perform a point-in-time to the latest time. At that time, you can select **Configure server** and change the backup to geo-redundant backup.

 * **How frequently is the backup copied to the remote region?** <br>
  Backups are shipped as soon as they are performed at the primary site. WAL files are also copied to the remote site as soon as possible. 

* **How do I perform geo-restore?** <br>
  You have to go through the create server process. During the process, you choose **Backup** as the source, which then lists all geo-redundant enabled server backups, along with the estimated point to which you can restore. You can optionally change the compute tier, backup type, and period as part of the create process.

* **What kind of RTO and RPO I can expect with geo-redundant backup?**  <br>
  Typically, you can expect up to 1 hour RPO (potential data loss). RTO (time to recover) depends on the size of the data to restore and how much data to recover.
 
 * **Can I do point-in-time recovery using the geo-redundant backup?** <br>
 No. Geo-restore does not allow you to chose a point in time. Instead, the restore targest the most recent geo-replicated backup, typically within the last hour. Restoring individual databases within a server is not supported.

 * **What is the difference between read replica and geo-backup/geo-restore?** <br>
  Both can be used for disaster recovery purposes. If you don't want to incur cost in having a running server at the server and you don't mind a longer downtime to restore the server, you can choose geo-redundant backup. If you have strict requirements for faster failover and reduced data loss, you can deploy read replica and fail over to that if you experience a disaster recovery event.

 * **Why I am not able to connect to my restored server?** <br>
  It's possible that you didn't change your server end point and/or the username to `username@new-restored-server-name` in your connection string.

## **Recommended Steps**

* If you try to restore a server in a different region and you're not seeing backups to restore from, make sure that the source server was created with geo-restore backups turned on
* If, after you access the new server, you see inconsistent data, confirm that the connection string (in particular, the user field: `username@servername`) references the new server
* The new server created during a restore doesn't have the firewall rules or VNet service endpoints that existed on the original server. These rules need to be set up separately for the new server. If you receive a `pg_hba` error, this indicates that your client's IP is not allowed for this server.
* Basic tier servers do not support geo-restore. 
* Review the [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity) to understand estimated restore times and restore point objectives
* Review the [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup) to understand supported functionality and regional coverage
* If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)

## **Recommended Documents**

* [Business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)
* [How-to restore a PostgreSQL server using Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)
