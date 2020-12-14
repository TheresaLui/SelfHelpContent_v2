<properties
    pageTitle="Troubleshoot query execution problems in Azure Database for PostgreSQL"
    description="Troubleshoot query execution problems in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="110"
    selfHelpType="generic"
    supportTopicIds="32640026, 32781014"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="89289f69-ddd4-4d91-9c70-06ed05412763"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshoot query execution problems in Azure Database for PostgreSQL

Query execution problems can be caused by the database engine itself or by the interaction of the database engine and the service. Follow the recommended steps to troubleshoot your problem.

## **Recommended Steps**

* Check your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.
* If you are experiencing issues such as timeouts or the loss of connectivity, check the [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues) documentation
* If you are experiencing slow query performance, check the [Performance Recommendations](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)

## **Recommended Documents**

* [Azure Database for PostgreSQL documentation](https://docs.microsoft.com/azure/postgresql/)<br>
* [Query Store](https://docs.microsoft.com/azure/postgresql/concepts-query-store)<br>
* [Query Performance Insights](https://docs.microsoft.com/azure/postgresql/concepts-query-performance-insight)<br>
* [Performance Recommendations](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)
