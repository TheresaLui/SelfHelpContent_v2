<properties
    pageTitle="Managing server parameters in Azure Database for PostgreSQL"
    description="Managing server parameters in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="490"
    selfHelpType="generic"
    supportTopicIds="32780952"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-server-modifyserverparameters"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing server parameters in Azure Database for PostgreSQL

Azure Database for PostgreSQL servers are created with default parameter values that balance performance and stability. Certain parameters can be reconfigured at the server level using the Azure portal or the Azure CLI.

Not all PostgreSQL parameters are available for you to reconfigure in Azure Database for PostgreSQL. If a PostgreSQL parameter is not listed in your server's Azure portal **Server parameters** window, then it cannot be reconfigured from the default.

To review the current list of configurable parameters, navigate to the **Server parameters** window in Azure portal. Several Postgres parameters require you to restart the server in order for them to take effect. These parameters are indicated by the property `Static`.

## **Recommended Steps**

* If a parameter that you'd like to configure isn't listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597976-azure-database-for-postgresql). We evaluate these requests periodically and we make parameters configurable if we can safely do so.
* Some PostgreSQL parameters can be modified at a session level using the PostgreSQL [`SET` command](https://www.postgresql.org/docs/current/sql-set.html). You can identify which parameters are session-level-modifiable using the SQL query: `SELECT name, context FROM pg_settings where context='user';`.
* The `shared_buffers` setting changes depending on the selected compute size

