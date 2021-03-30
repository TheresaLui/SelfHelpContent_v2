<properties
    pageTitle="Automated backups in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Automated backups"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32639968, 32780979"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8d101db0-cc7c-4c31-a9da-3f85bf9c063d"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Automated backups in Azure Database for PostgreSQL - Single Server

Most users can resolve issues related to automated backups by using the following information.

## Frequently asked questions

* **At what frequency my server backups are done?** <br>
  Azure Database for PostgreSQL automatically takes backups of your server. 
  - For maximum supported storage with a size of < 4 TB, full backups occur weekly and differential backups occur twice a day for servers. 
  - For 16 TB storage, snapshot backups happen at least once a day for each server. 
  - Transaction log backups in both cases occur every five minutes. 
  
* **Where are backups are stored?** <br>
  The backups are stored on regular disks and Azure Blob storage. 

* **What is the backup retention period that is supported?** <br>
  The default and minimum retention period for backups is 7 days and can be increased up to 35 days. You can perform local point-in-time recovery to any time within the retention period.

* **Can I configure long-term retention for more than 35 days?** <br>
  You can choose [Azure Backup for PostgreSQL - Preview](https://docs.microsoft.com/azure/backup/backup-azure-database-postgresql) for storing long-term backup. 

* **Can I do on-demand backup?** <br>
   The service does not allow on-demand backups from Azure portal or CLI. You can perform `pg_dump` from your client. 

* **How do I know if the backup is performed or not?** <br>
   Azure Database for PostgreSQL is a managed service that takes care of typical management tasks like doing regular backups. The service is responsible for adhering to your retention requirements and storing all the relevant backup data and WAL files. We have internal mechanisms that trigger internal tickets in the event of any issues with taking backups, and we fix these issues. 

* **How can I verify the backup?** <br>
  You can periodically verify backup by performing point-in-time recovery and checking the data.

* **Can I restore only a specific database or table?** <br>
   No. As the backup happens at the server level, all databases and all their objects are restored. To restore only a specific database or table, you can then export only that data from the restored server and copy it to your production server. 

* **How does the point-in-time work?** <br>
  A new server is first provisioned. Then, based on the time of restore requested, the backup is restored, along with WAL files. Then the recovery is performed until the time requested.

* **Why I am not able to connect to my restored server?** <br>
  It is possible that you may not have changed your server end point and/or the user name to `username@new-restored-server-name` in your connection string.

* **What backup storage metrics are available?** <br>
  Servers that can scale up to 16 TB do not yet have a backup storage metric available. Backups are being taken for these servers, as described above. Work is in progress to provide a backup storage metric.

* **Can I use the automatic backups to restore on my VM?** <br>
    No. These backup files cannot be exported and can only be used for restores in-service. If you want to export the PostgreSQL database, review the [How-to export PostgreSQL database using pg_dump](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import) steps.

* **How much does the backup storage cost?** <br>
    Azure Database for PostgreSQL provides up to 100 percent of your provisioned server storage size as backup storage at no additional cost. Typically, this corresponds to a backup retention of 7 days. You can track this storage with the metric Backup Storage Used. Storage consumed for backups in excess of the provisioned server storage size is charged according to the [pricing model](https://azure.microsoft.com/pricing/details/postgresql/).

* **Why my backup storage is increasing unexpectedly, even though there's no big change to my database size?** <br>
   If you have an increased number of transactions in your database, this increases the number of transactions logged. In turn, the transaction log backups also become larger. Because these backups are retained until they pass your selected retention days, you may see an elevated backup usage size. 

## **Recommended Steps**

* Azure Database for PostgreSQL supports point-in-time restore to any point within the configured backup retention period for a server. The restore operation will create a new server side-by-side with the old server. In-place restores and restoring individual databases within a server are not supported.

* The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically and users do not have access to the backups. Because transaction log backups are taken every 5 minutes, you may need to wait 5 minutes before you're able to restore to a specific point-in-time within a 5 minute interval.

* If you are having connectivity issues after restoring the server, make sure that the connection string refers to the restored server and that the username has the servername of the restored server in the `username@servername` for Single server. In case of Flexible server, simply use the `username` on the restored server.

* If you are trying to restore to a point-in-time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again.

* The point-in-time restore duration depends on your database size and the transaction log size from the last full backup. The restore operation can take up to 12 hrs and depends on multiple factors, including storage provisioned and ongoing transactions on the server.
  
## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [How-to restore a PostgreSQL server using Azure portal](https://docs.microsoft.com/azure/postgresql/howto-restore-server-portal)<br>
* [How-to restore a PostgreSQL server using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-restore-server-cli)<br>
* [How-to export PostgreSQL database using `pg_dump`](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-export-and-import)
