<properties
	pageTitle="Troubleshooting query performance in Azure Database for MySQL"
	description="Troubleshooting query performance in Azure Database for MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="31"
	selfHelpType="resource"
	supportTopicIds="32628404, 32628397"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="1f8be777-e8a7-4e21-8c28-40baaa6fe4a2"
/>

# Troubleshooting query performance in Azure Database for MySQL

Query performance issues can have many different root causes. Work through the recommended steps to solve most common causes for performance issues.

## **Recommended Steps**

* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload utilize all the resources
* Only retrieve the columns you really need instead of using *select \**
* Assure you have the right set of indexes created for you queries

## **Recommended Documents**

* [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance)<br>
* [How-to use sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema)
