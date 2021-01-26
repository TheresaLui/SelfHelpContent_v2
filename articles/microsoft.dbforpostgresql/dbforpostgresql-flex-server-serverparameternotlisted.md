<properties
    pageTitle="Server parameter not listed"
    description="Guidance on what to do when a server parameter is not listed"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="500"
    selfHelpType="generic"
    supportTopicIds="32780954"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-server-serverparameternotlisted"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server parameter not listed

Azure Database for PostgreSQL servers are created with default parameter values that balance performance and stability. Certain parameters can be reconfigured at the server level using the Azure portal or the Azure CLI.

Not all PostgreSQL parameters are available for you to reconfigure in Azure Database for PostgreSQL. If a PostgreSQL parameter is not listed in your server's Azure portal **Server parameters** window, it cannot be reconfigured from the default.

To review the current list of configurable parameters, navigate to the **Server parameters** window in the Azure portal. A few Postgres parameters require you to restart the server for them to take effect. These are indicated by the property `Static`.

## **Recommended Steps**

* If a parameter you'd like to configure is not listed, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597976-azure-database-for-postgresql). We evaluate these requests periodically and make parameters configurable if we can safely do so.
* Some PostgreSQL parameters can be modified at a session level using the PostgreSQL [`SET` command](https://www.postgresql.org/docs/current/sql-set.html). You can identify which parameters are session-level-modifiable using the SQL query: `SELECT name, context FROM pg_settings where context='user';`.
* The `shared_buffers` setting changes, depending on the selected compute size

