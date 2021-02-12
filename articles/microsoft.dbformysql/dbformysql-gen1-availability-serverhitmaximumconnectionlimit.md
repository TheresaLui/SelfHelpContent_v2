<properties
    pageTitle="Connection limits in Azure Databases for MySQL Single Server"
    description="Connection limits in Azure Databases for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32747586"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="960408d0-b58f-4704-bb9c-6d0ff057158e"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection limits in Azure Databases for MySQL Single Server

Azure Database for MySQL Single Server has a fixed limit of maximum allowed concurrent connections. This limit depends on the compute resources provisioned for your server. The current max number of connections are published in the [server parameters](https://docs.microsoft.com/azure/mysql/concepts-server-parameters) article.

## **Recommended Steps**

* Review the [Single server max connection limits](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#max_connections) and scale your server to the right size to handle the workload
* Investigate if all connections are actually used, or is some are idle. Closing idle connections and ideally using connection pooling help optimize the number of concurrent connections.

## **Recommended Documents**

* [Azure Database for MySQL Single Server - Service limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)