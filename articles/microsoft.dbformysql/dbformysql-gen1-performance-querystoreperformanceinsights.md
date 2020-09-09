<properties
    pageTitle="Troubleshooting query insights performance insights in Azure Database for MySQL Single Server"
    description="Troubleshooting query insights performance insights in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="250"
    selfHelpType="generic"
    supportTopicIds="32747578"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b54badaa-461e-4bd8-97f4-a2184a87d7a1"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting query performance in Azure Database for MySQL Single Server

Query performance issues can have many different root causes. Work through the recommended steps to solve for the most common causes for performance issues.

## **Recommended Steps**

* Use our intelligent performance features for additional insights:

  * [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store)
  * [Query Performance Insights](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
  * [Performance Recommendations](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)

* If you want to use Query Store, ensure that **default_transaction_read_only** is not set to ON. Assure you have the right set of indexes created for your queries
* Make sure that the [limitations](https://docs.microsoft.com/azure/mysql/concepts-query-store#limitations-and-known-issues) are not hit.

## **Recommended Documents**

*   [Query store documentation](https://docs.microsoft.com/azure/mysql/concepts-query-store)
*   [Query performance insights documentation](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)