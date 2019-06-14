<properties
	pageTitle="Troubleshooting login performance in Azure Database for MySQL"
	description="Troubleshooting login performance in Azure Database for MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="30"
	selfHelpType="resource"
	supportTopicIds="32640061"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="bf6e9142-c4eb-447c-99b6-c0a0d7e9ca94"
/>

# Troubleshooting login performance in Azure Database for MySQL

Slow login issues can have many different root causes. Work through the recommended steps to solve the most common performance issues.

## **Recommended Steps**

* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload utilize all the resources
* Turn on accelerated networking for lowest connection latency when connecting from an Azure virtual machine
* Use connection pooling on the client

## **Recommended Documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
