<properties
    pageTitle="Troubleshoot query execution problems in Azure Database for MariaDB"
    description="Troubleshoot query execution problems in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="110"
    selfHelpType="generic"
    supportTopicIds="32640157"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="774289b1-c59b-4777-ac81-03f275afa4ff"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Troubleshoot query execution problems in Azure Database for MariaDB

Query execution problems can be caused by the database engine itself or by the interaction of the database engine and the service. Follow the recommended steps to troubleshoot your problem.

## **Recommended Steps**

* Check your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.  Check  [Monitoring in Azure Database for MariaDb](https://docs.microsoft.com/azure/mariadb/concepts-monitoring) documentation.
* If you are experiencing issues such as timeouts or the loss of connectivity, check the [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues) documentation
* If you are experiencing slow query performance, check the [Troubleshoot query performance in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-query-performance) documentation
* Search the internet for solutions from the MariaDB community

## **Recommended Documents**

* [Monitor and tune](https://docs.microsoft.com/azure/mariadb/concepts-monitoring/)<br>
* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
