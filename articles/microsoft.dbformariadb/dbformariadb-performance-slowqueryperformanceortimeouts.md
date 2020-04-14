<properties
    pageTitle="Troubleshooting query performance in Azure Database for MariaDB"
    description="Troubleshooting query performance in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="90"
    selfHelpType="generic"
    supportTopicIds="32640156"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="badb04d0-4b9d-40e2-98db-d746e36302e4"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Troubleshooting query performance in Azure Database for MariaDB

Query performance issues can have many different root causes. Work through the recommended steps to solve for the most common causes for performance issues.

## **Recommended Steps**

* Review [Troubleshoot query performance in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-query-performance)
* Use our intelligent performance features for additional insights:

  * [Query Store](https://docs.microsoft.com/azure/mariadb/concepts-query-store)
  * [Query Performance Insights](https://docs.microsoft.com/azure/mariadb/concepts-query-performance-insight)
  * [Performance Recommendations](https://docs.microsoft.com/azure/mariadb/concepts-performance-recommendations)

* Assure you have the right set of indexes created for your queries
* Make sure that there are no deadlocks in the concurrent queries
* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.
* Only retrieve the columns you really need instead of using `select \*`

## **Recommended Documents**

* [Monitor and tune](https://docs.microsoft.com/azure/mariadb/concepts-monitoring/)<br>
* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
