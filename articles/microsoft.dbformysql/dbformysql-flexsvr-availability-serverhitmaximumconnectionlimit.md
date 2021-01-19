<properties
    pageTitle="Connection limits in Azure Databases for MySQL Flexible Server"
    description="Connection limits in Azure Databases for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32747638"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="77d279a7-7572-4dd8-bf9d-a2449ebde123"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection limits in Azure Databases for MySQL Flexible Server

Azure Database for MySQL Flexible Server has a fixed limit of maximum allowed concurrent connections. This limit depends on the compute resources provisioned for your server. The current max number of connections are published in the [service limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)

## **Recommended Steps**

* Flexible server max connection limits can be calculated using the formula: `2 * {Memory (in bit)} / 12582880`
  * Refer to the [compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage) document to learn more about memory allocated per compute size
* If you are hitting max connection limits, scale your server to the right size to handle the workload
* Investigate if all connections are actually used, or is some are idle. Closing idle connections and ideally using connection pooling help optimize the number of concurrent connections.

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server - Service limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)