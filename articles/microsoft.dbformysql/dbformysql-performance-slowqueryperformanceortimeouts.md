<properties
    pageTitle="Troubleshooting query performance in Azure Database for MySQL"
    description="Troubleshooting query performance in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="90"
    selfHelpType="generic"
    supportTopicIds="32640094"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="69a504ec-67e1-4d7a-ad2f-46ec95ca044a"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting query performance in Azure Database for MySQL

Query performance issues can have many different root causes. Work through the recommended steps to solve for the most common causes for performance issues.

## **Recommended Steps**

* Review [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance)
* Analyze your workload using [sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema)
* Use our intelligent performance features for additional insights:

  * [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store)
  * [Query Performance Insights](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
  * [Performance Recommendations](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)

* Assure you have the right set of indexes created for your queries
* Make sure that there are no deadlocks in the concurrent queries
* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.
* Only retrieve the columns you really need instead of using `select \*`

## **Recommended Documents**

* [Monitor and tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring)<br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
