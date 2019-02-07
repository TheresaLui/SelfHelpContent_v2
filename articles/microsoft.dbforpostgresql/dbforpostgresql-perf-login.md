<properties
	pageTitle="Troubleshooting login performance in Azure Database for PostgreSQL"
	description="Troubleshooting login performance in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="30"
	selfHelpType="resource"
	supportTopicIds="32628457"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="46d2f88a-161c-49f3-a847-c45c4e6bd47c"
/>

# Troubleshooting login performance in Azure Database for PostgreSQL

Slow login issues can have many different root causes. Work through the recommended steps to solve the most common performance issues.

## **Recommended Steps**

* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload utilize all the resources
* Turn on accelerated networking for lowest connection latency when connecting from an Azure virtual machine
* Use connection pooling on the client

## **Recommended Documents**

* [Azure Database for PostgreSQL documentation](https://docs.microsoft.com/azure/postgresql/)
