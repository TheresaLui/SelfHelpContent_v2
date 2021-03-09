<properties
    pageTitle="Dropped server in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: deleted server"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="170"
    selfHelpType="generic"
    supportTopicIds="32780975"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-backup-recoveradroppedresource"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Restoring a deleted server

Azure Database for PostgreSQL generally does not support restoring a deleted server. When a server is deleted, the operation cascades to the backups shortly after the server delete operation is initiated.

## **Recommended Steps**

* If you accidentally drop a server, immediately issue a point-in-time restore request using our REST API to a point in time just before the time the server was dropped. You can issue this request within 7 days of accidentally dropping a server. This may enable you to recover the deleted server.
* In the future, consider [using a lock](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/prevent-the-disaster-of-accidental-deletion-for-your-postgres/ba-p/825196) to prevent accidental deletions
