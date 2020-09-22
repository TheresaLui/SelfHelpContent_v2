<properties
    pageTitle="Connection limits in Azure Databases for PostgreSQL"
    description="Connection limits in Azure Databases for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="10"
    selfHelpType="generic"
    supportTopicIds="32640018"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e4163dda-50db-4176-bf65-0bc5bdeae459"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Connection limits

Each Azure Database for PostgreSQL server has a maximum number of allowed connections. This maximum is predetermined by taking into account the amount of memory available for your server. This is based on the service tier and the number of vCores provisioned for your server. The connection limits are published in the [documentation](https://docs.microsoft.com/azure/postgresql/concepts-limits).

When connections exceed the limit, you may receive an error:
`FATAL: sorry, too many clients already`

## **Recommended Steps**

* Review the [max connection limits](https://docs.microsoft.com/azure/postgresql/concepts-limits) and scale your server up if you want more connections. 
* Investigate if all connections are actually used, or if some are idle. To check, query [pg_stat_activity](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Connection-handling-best-practice-with-PostgreSQL/ba-p/790883). 
   - Idle connections occupy memory in Postgres. Close idle connections to free up room for new connections. 
   - Consider using a server side [connection pooler such as pgbouncer](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Steps-to-install-and-setup-PgBouncer-connection-pooling-proxy/ba-p/730555) to help optimize the number of concurrent connections.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
