<properties
	pageTitle="Troubleshooting query performance in Azure Database for PostgreSQL"
	description="Troubleshooting query performance in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="16"
	selfHelpType="resource"
	supportTopicIds="32640025"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="MoonCake"
	articleId="fd54f6b6-653f-460f-88ba-d8350893e55a"
/>

# Troubleshooting query performance in Azure Database for PostgreSQL

Query performance issues can have many different root causes. Work through the following recommended steps to solve most common performance issues.

## **Recommended Steps**

* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload utilize all the resources
* Only retrieve the columns you really need instead of using *select \**

## **Recommended Documents**

* [How-to optimize bulk inserts](https://docs.azure.cn/postgresql/howto-optimize-bulk-inserts)
* [How-to optimize auto vacuum](https://docs.azure.cn/postgresql/howto-optimize-autovacuum)
* [How-to optimize query stats collection](https://docs.azure.cn/postgresql/howto-optimize-query-stats-collection)
* [How-to optimize your toast table strategy](https://docs.azure.cn/postgresql/howto-optimize-query-time-with-toast-table-storage-strategy)
