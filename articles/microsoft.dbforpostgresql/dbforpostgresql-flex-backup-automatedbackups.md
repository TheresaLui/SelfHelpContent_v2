<properties
    pageTitle="Automated backups in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Automated backups"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32780969"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-backup-automatedbackups"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Automated backups
Azure Database for PostgreSQL - Flexible Server performs automated backups of your database server. It also allows you to perform point-in-time restore of your server. You may be able to find answers to most of your backup and restore related questions.

## Frequently asked questions

* **What should I do to configure flexible server to perform backups of my server?** <br>
By default, flexible server performs automatic backups of your server. By default, 7 days of retention is provided. You can configure the retention period up to 35 days at the time of server provisioning or at a later time. 

* **Can I choose not to enable backup for my server - as that is for testing only?** <br>
No. All servers are configured to have backups taken.

* **Is the backup performed at the server-level or the database-level?** <br>
The backup is performed at the server level, including all the databases. You cannot choose to backup specific database. You can always use pg_dump to backup only the database.

* **Can I restore to any point-in-time?** <br>
Yes. You can choose to either restore to the latest data (default) or to any point-in-time within the retention period.

* **How are backups performed and retained?** <br>
Data volumes are backed up using daily storage snapshots. WAL files are archived continuously. Data and WAL backups are retained to satisfy the retention window.

* **Can I restore my backup to another AZ in the event of my primary AZ outage?** <br>
Yes. The backup data by default is stored in zone-redundant mode. So, you will be able to restore the server in a different AZ within that region.

* **Can I restore to the same server?** <br>
No. To avoid accidental over-writing, restored servers are always restored to a new name.

* **How do I restore a specific database or table?** <br>
You can perform the PITR to a new server. Then from your PostgreSQL client or using AZ CLI from the portal, you can do dump of the database or the table and import into your server.

* **Can I use the backup to restore for DR purpose in the event of region-level failover?** <br>
No. Backups are confined to a region. In future, when we support Geo-backup, you can then use the backup to restore on a different region for DR purpose.

* **How long does it take to perform PITR?** <br>
It typically depends on factors including the data backup taken before the requested point-in-time and the amount of recovery to be performed post the data restore. It can be anywhere between few minutes to few hours.

* **How do I see how much backup data storage is consumed?** <br>
You can check the metrics to see backup storage utilization.

* **How much does it cost for storing backup?** <br>
You are charged only if the backup size of the server exceeds the provisioned size of the database server. Please refer to the pricing page. You can monitor the metrics to see the backup storage utilization.

* **My database is small. But I see huge increase in backup storage. Why?** <br>
The backup consists of both data and logs (WAL). Even though the data is small, if you do a lot of changes, WAL size will keep increasing and when those are backed up, the backup size increases. If you are running into the backup size issue, please check your writes and changes to the database. You can monitor write IOPS and throughput and also WAL from server metrics.

* **Can I configure long-term retention for more than 35 days?** <br>
The service does not offer a managed way to retain backups for long term. However, you can perform dump of your databases and store it on a different storage or Azure blob.  


## **Recommended Steps**

* Configure the retention period to suit your application and business needs.
* Monitor for backup storage usage to avoid 

## **Reference documents**

* [Flexible server - Backup & Restore](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-backup-restore)
* [Flexible server - Business Continuity](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-business-continuity)
* 
* 
* 




