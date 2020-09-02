<properties
    pageTitle="Automated backups in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Automated backups"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="140"
    selfHelpType="generic"
    supportTopicIds="32639968"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-backup-automatedbackups"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Automated backups

Azure Database for PostgreSQL automatically takes backups of your server. The backups are used to support the point-in-time restore features.

You can choose to take a dump of a database on your server using pg_dump.

## **Recommended Steps**

* Restore operations in flexible server create a new database server and do not overwrite the existing database server.

* You can use the *Backup storage used* metric in the Azure portal to monitor the backup storage consumed by a server. The Backup Storage used metric represents the sum of storage consumed by all the database backups and log backups retained based on the backup retention period set for the server. Heavy transactional activity on the server can cause backup storage usage to increase irrespective of the total database size.
