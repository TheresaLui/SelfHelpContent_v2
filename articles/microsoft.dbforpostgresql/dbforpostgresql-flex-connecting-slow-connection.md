<properties
    pageTitle="Connection taking longer to connect to PostgreSQL"
    description="Connection taking longer to connect to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32789524"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9ac49f4e-7224-438c-8745-3b9171b7da8c"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Taking longer to establish connection with the PostgreSQL Server**
## **Recommended Steps**

Establishing a new connection takes compute and memory resources which can impact your production workload. It is always a good practice to manage the connections efficiently when possible

- If there are many concurrent short duration connections. For example, application with high level of concurrency, creates a connection for each interaction with the database, runs a simple query, and then closes the connection. 
- If there is sudden influx of new connections. For example, when the database server is restarted by users or after the scheduled maintenance is completed or at the start of business peak hours. As a best practice, we highly recommend using [connection pooling](https://azure.microsoft.com/blog/performance-best-practices-for-using-azure-database-for-postgresql-connection-pooling/).
- Flexible Server provides a built-in option to pool connections using integrated PgBouncer for General Purpose and Memory Optimized tiers. You can just enable it and connect to the Server using Port 6432

## **Recommended Documents**

- [Quickstart: Connect and query with Azure CLI with Azure Database for PostgreSQL - Flexible Server](https://docs.microsoft.com/azure/postgresql/flexible-server/connect-azure-cli)
