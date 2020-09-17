<properties
    pageTitle="Connection issues to Azure Databases for MySQL"
    description="Connection issues to Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="10"
    selfHelpType="generic"
    supportTopicIds="32640090"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="064e5cc6-7e43-4a21-810c-49d92c4834d0"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection limits in Azure Databases for MySQL

Both Azure Database for MySQL Single Server and Flexible Server have a fixed limit of maximum allowed concurrent connections. This limit depends on the compute resources provisioned for your server. The current max number of connections are published in the respective documents: [Single server](https://docs.microsoft.com/azure/mysql/concepts-server-parameters) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server).

## **Recommended Steps**

* Review the [Single server max connection limits](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#max_connections) and scale your server to the right size to handle the workload
* Flexible server max connection limits can be calculated using the formula: `2 * {Memory (in bit)} / 12582880`
  * Refer to the [compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage) document to learn more about memory allocated per compute size
* Investigate if all connections are actually used, or is some are idle. Closing idle connections and ideally using connection pooling help optimize the number of concurrent connections.

## **Recommended Documents**

* [Azure Database for MySQL Single Server - Service limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)<br>
* [Azure Database for MySQL Flexible Server - Service limitations](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-limitations)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)