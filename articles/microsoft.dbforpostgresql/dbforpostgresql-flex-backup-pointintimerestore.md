<properties
    pageTitle="Point-in-time restore in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL:point-in-time restore"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32780974"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-backup-pointintimerestore"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Point-in-time restore
Azure Database for PostgreSQL - Flexible Server performs automated backups of your database server. It also allows you to perform point-in-time restore of your server. You may be able to find answers to most of your backup and restore related questions.

## Frequently asked questions

* **Can I restore to any point-in-time?** <br>
Yes. You can choose to either restore to the latest data (default) or to any point-in-time within the retention period.

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

* **Can I configure long-term retention for more than 35 days?** <br>
The service does not offer a managed way to retain backups for long term. However, you can perform dump of your databases and store it on a different storage or Azure blob.  


## **Recommended Steps**

* Ensure that the point in time that you're trying to restore is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point \-in-time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again.

## **Reference documents**

* [Flexible server - Backup & Restore](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-backup-restore)
* [Flexible server - Business Continuity](https://docs.microsoft.com/azure/postgresql/flexible-server/concepts-business-continuity)



