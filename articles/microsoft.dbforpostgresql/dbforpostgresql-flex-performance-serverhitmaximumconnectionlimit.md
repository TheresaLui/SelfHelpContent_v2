<properties
    pageTitle="Troubleshooting maximum connection limit in Azure Database for PostgreSQL"
    description="Troubleshooting maximum connection limit in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="60"
    selfHelpType="generic"
    supportTopicIds="32781009"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-serverhitmaximumconnectionlimit"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting maximum connection limit in Azure Database for PostgreSQL

Each active connection consumes memory. Therefore, the maximum number of connections allowed depends on the chosen pricing tier. Higher pricing tiers have more memory and therefore, higher limits on maximum connections. If you see the error messages, "Remaining connection slots are reserved for non-replication superuser connections" or "FATAL: sorry, too many clients already", you are likely hitting a maximum connection limit.

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a connection pooler such as PgBouncer to manage connections
* Make sure that you have chosen a compute tier that can support the maximum number of connections required by the application

