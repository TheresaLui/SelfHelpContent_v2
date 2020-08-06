<properties
    pageTitle="Troubleshoot query execution problems in Azure Database for MySQL"
    description="Troubleshoot query execution problems in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="110"
    selfHelpType="generic"
    supportTopicIds="32640095"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="449f5c2d-d791-4b88-b7e1-78ccf5af4a01"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshoot query execution problems in Azure Database for MySQL

Query execution problems can be caused by the database engine itself or by the interaction of the database engine and the service. Follow the recommended steps to troubleshoot your problem.

## **Recommended Steps**

* Check your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on. Check  [Monitoring in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-monitoring) documentation.
* If you are experiencing issues such as timeouts or the loss of connectivity, check the [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues) documentation
* If you are experiencing slow query performance, check the [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance) documentation
* Search the internet for solutions from the MySQL community

## **Recommended Documents**

* [How-to use sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema)<br>
* [Monitor and tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring/)<br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
