<properties
    pageTitle="Long term retention of backups for Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Long term retention"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32780972"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-backup-longtermbackupretention"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Long term retention of backups

## **Recommended Steps**
Long-term retention of backups (longer than 35 days) are currently not natively supported by the service. You have the option to use *pg_dump* to take backups and store them for long-term retention. Third-party solutions are another option.

Native support for long-term retention backups is currently being worked on by the Azure engineering team.
