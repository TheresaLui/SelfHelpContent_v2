<properties
	pageTitle="Troubleshooting query performance in Azure Database for PostgreSQL"
	description="Troubleshooting query performance in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="31"
	selfHelpType="resource"
	supportTopicIds="32628454, 32628447"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="fd54f6b6-653f-460f-88ba-d8350893e55a"
/>

# Troubleshooting query performance in Azure Database for PostgreSQL

Query performance issues can have many different root causes. Work through the following recommended steps to solve most common performance issues.

## **Recommended Steps**

* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload utilize all the resources
* Only retrieve the columns you really need instead of using *select \**
* Check if there were changes in your query execution times over time using [Query Performance Insights](https://docs.microsoft.com/azure/postgresql/concepts-query-performance-insight)
* Assure you have the right set of indexes created for you queries, see if you have index recommendation in our [Performance Recommendations](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)

## **Recommended Documents**

* [How-to optimize bulk inserts](https://docs.microsoft.com/azure/postgresql/howto-optimize-bulk-inserts)<br>
* [How-to optimize auto vacuum](https://docs.microsoft.com/azure/postgresql/howto-optimize-autovacuum)<br>
* [How-to optimize query stats collection](https://docs.microsoft.com/azure/postgresql/howto-optimize-query-stats-collection)<br>
* [How-to optimize your toast table strategy](https://docs.microsoft.com/azure/postgresql/howto-optimize-query-time-with-toast-table-storage-strategy)
