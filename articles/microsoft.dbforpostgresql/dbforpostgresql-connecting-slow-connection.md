<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32788704, 32789530"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="beacf2c0-fe59-4812-821a-05072c5bbe49"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Taking longer to establish connection with the PostgreSQL Server**
## **Recommended Steps**

Due to the architectural choice in Single Server PostgreSQL, creating a new connection is a resource (CPU) intensive operation and can take roughly 200-400 milliseconds. This can impact your workload performance. Many customers especially when they migrate the PostgreSQL database from on-premise, or IaaS (VM) or from competitive public cloud to Azure PostgreSQL experience a slowdown in the application. The common scenarios where customers have experienced a slowdown are listed below along with recommended best practice 

- If there are many concurrent short duration connections. For example, application with high level of concurrency, creates a connection for each interaction with the database, runs a simple query, and then closes the connection. 
- If there is sudden influx of new connections. For example, when the database server is restarted by users or after the scheduled maintenance is completed or at the start of business peak hours. As a best practice, we highly recommend using [connection pooling](https://azure.microsoft.com/blog/performance-best-practices-for-using-azure-database-for-postgresql-connection-pooling/).

## **Recommended Documents**

- [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
- [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
