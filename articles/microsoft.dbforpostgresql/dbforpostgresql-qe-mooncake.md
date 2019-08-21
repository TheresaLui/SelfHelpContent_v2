<properties
	pageTitle="Troubleshoot query execution problems in Azure Database for PostgreSQL"
	description="Troubleshoot query execution problems in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="17"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servers, databases"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="dbforpostgresql-qe-mooncake"
/>

# Troubleshoot query execution problems in Azure Database for PostgreSQL

Query execution problems can because by the database engine itself or by the interaction of the database engine and the service. Work through the following recommended steps for a first level of troubleshooting.

## **Recommended Steps**

* Check your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload max out the available resources
* If you are experiencing issues such as timeouts or the loss of connectivity, check the [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.azure.cn/postgresql/howto-troubleshoot-common-connection-issues) documentation
* Reach out to the PostgreSQL community on the internet for possible solutions

## **Recommended Documents**

* [Query Store](https://docs.azure.cn/postgresql/concepts-query-store)
* [How-to optimize bulk inserts](https://docs.azure.cn/postgresql/howto-optimize-bulk-inserts)
* [How-to optimize auto vacuum](https://docs.azure.cn/postgresql/howto-optimize-autovacuum)
* [How-to optimize query stats collection](https://docs.azure.cn/postgresql/howto-optimize-query-stats-collection)
* [How-to optimize your toast table strategy](https://docs.azure.cn/postgresql/howto-optimize-query-time-with-toast-table-storage-strategy)
