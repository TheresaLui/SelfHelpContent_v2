<properties
	pageTitle="Troubleshoot query execution problems in Azure Database for MySQL"
	description="Troubleshoot query execution problems in Azure Database for MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="40"
	selfHelpType="resource"
	supportTopicIds="32628411, 32628398, 32628373"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="85d309a2-e0b3-45ae-9b00-c24bee599451"
/>

# Troubleshoot query execution problems in Azure Database for MySQL

Query execution problems can because by the database engine itself or by the interaction of the database engine and the service. 

## **Recommended Steps**

* Check your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server and increase your I/O and or compute resources should your workload max out the available resources
* If you are experiencing issues such as timeouts or the loss of connectivity, check the [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues) documentation
* If you are experiencing slow query performance, check the [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance) documentation
* Search the internet for solutions from the MySQL community

## **Recommended Documents**

* [How-to use sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema)<br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
