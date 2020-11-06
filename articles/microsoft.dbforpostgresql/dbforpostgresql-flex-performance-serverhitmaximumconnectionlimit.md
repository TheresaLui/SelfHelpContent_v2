<properties
    pageTitle="Troubleshooting maximum connection limit in Azure Database for PostgreSQL"
    description="Troubleshooting maximum connection limit in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="60"
    selfHelpType="generic"
    supportTopicIds="32640019, 32781010"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-serverhitmaximumconnectionlimit"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting maximum connection limit in Azure Database for PostgreSQL

Each active connection consumes memory and therefore the maximum number of connections allowed depends upon the chosen pricing tier. Higher pricing tiers have more memory and hence higher limits on maximum connections. If you see the error "remaining connection slots are reserved for non-replication superuser connections" or "FATAL: sorry, too many clients already", you are likely hitting a max connection limit.

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a connection pooler like PgBouncer to manage connections
* Ensure you have chosen a compute tier that can support the maximum number of connections required by the application

