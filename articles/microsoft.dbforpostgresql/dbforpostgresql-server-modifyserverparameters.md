<properties
    pageTitle="Managing server parameters in Azure Database for PostgreSQL"
    description="Managing server parameters in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="490"
    selfHelpType="generic"
    supportTopicIds="32639997"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c2ef1831-8aaf-41b4-b8a9-ad7d62ef91ef"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing server parameters in Azure Database for PostgreSQL

Azure Database for PostgreSQL servers are created with default parameter values that balance performance and stability. Certain parameters can be reconfigured at the server level using the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal) or the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-cli). 

Not all PostgreSQL parameters are available for you to reconfigure in Azure Database for PostgreSQL. If a PostgreSQL parameter is not listed in your server's Azure portal **Server parameters** window, then it cannot be reconfigured from the default.

To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal. A few Postgres parameters require you to restart the server for them to take effect. These are indicated by the property 'Static'.

## **Recommended Steps**

* If a parameter you'd like to configure is not listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597976-azure-database-for-postgresql). We evaluate these requests periodically and make parameters configurable if we can safely do so.
* Query Performance Insights, Performance Recommendations do not work for read replica servers. Query Store for read replica servers contains a copy of the master server's data. 
* Some PostgreSQL parameters can be modified at a session level using the PostgreSQL [SET command](https://www.postgresql.org/docs/current/sql-set.html). You can identify which parameters are session-level-modifiable using the SQL query: `SELECT name, context FROM pg_settings where context='user';`.
* If there is a change in the server's parameter value from the portal, sometime the client does not see the parameter changed. In such cases client need to reconnect to take param effect after updating param on portal.
* The 'shared_buffers' setting changes depending on the selected sku (sku determines the memory available). General Purpose servers have 2GB shared_buffers for 2 vCores; Memory Optimized servers have 4GB shared_buffers for 2 vCores. The shared_buffers setting scales linearly (approximately) as vCores increase in a tier.

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-cli)
