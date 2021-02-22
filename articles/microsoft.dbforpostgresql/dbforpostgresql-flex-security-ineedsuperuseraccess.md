<properties
    pageTitle="Managing permissions in Azure Database for PostgreSQL servers"
    description="Managing permissions in Azure Database for PostgreSQL servers"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="480"
    selfHelpType="generic"
    supportTopicIds="32780939"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-security-ineedsuperuseraccess"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing permissions on in Azure Database for PostgreSQL servers

Each Azure Database for PostgreSQL server is created with a highly privileged admin role. User permissions for other users that you create are managed through the PostgreSQL built-in user management capabilities. 

**Note:** Superuser access cannot be granted to you in the managed service.

## **Recommended Steps**

* If you lose your admin account password, you can reset the password on your server's portal page
