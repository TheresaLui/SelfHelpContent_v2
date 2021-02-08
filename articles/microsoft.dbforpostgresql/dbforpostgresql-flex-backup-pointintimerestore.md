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

In Flexible Server, performing a point-in-time restore creates a new server from the flexible server's backups in the same region as your source server. It is created with the source server's configuration for the pricing tier, compute generation, compute, storage size, backup retention period, and backup redundancy option. Also, tags and settings such as VNet and firewall settings are inherited from the source server.

## **Recommended Steps**

* Ensure that the point in time that you're trying to restore is within your configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point \-in-time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again
