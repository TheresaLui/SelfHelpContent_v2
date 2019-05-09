<properties
	pageTitle="Troubleshoot query execution problems in Azure Database for PostgreSQL"
	description="Troubleshoot query execution problems in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="40"
	selfHelpType="resource"
	supportTopicIds="32640026, 32640027"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="a6322fae-939f-4909-845d-643f3599aa63"
/>

# Troubleshoot query execution problems in Azure Database for PostgreSQL

Query execution problems can because by the database engine itself or by the interaction of the database engine and the service. Work through the following recommended steps for a first level of troubleshooting.

## **Recommended Steps**

* Check your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload max out the available resources
* If you are experiencing issues such as timeouts or the loss of connectivity, check the [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues) documentation
* Search the internet for solutions from the PostgreSQL community

## **Recommended Documents**

* [Query Store](https://docs.microsoft.com/azure/postgresql/concepts-query-store)<br>
* [Query Performance Insights](https://docs.microsoft.com/azure/postgresql/concepts-query-performance-insight)<br>
* [Performance Recommendations](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)<br>
* [How-to optimize bulk inserts](https://docs.microsoft.com/azure/postgresql/howto-optimize-bulk-inserts)<br>
* [How-to optimize auto vacuum](https://docs.microsoft.com/azure/postgresql/howto-optimize-autovacuum)<br>
* [How-to optimize query stats collection](https://docs.microsoft.com/azure/postgresql/howto-optimize-query-stats-collection)<br>
* [How-to optimize your toast table strategy](https://docs.microsoft.com/azure/postgresql/howto-optimize-query-time-with-toast-table-storage-strategy)
