<properties
    pageTitle="Connection issues to Azure Databases for MySQL"
    description="Connection issues to Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="10"
    selfHelpType="generic"
    supportTopicIds="32640090"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="064e5cc6-7e43-4a21-810c-49d92c4834d0"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection issues to Azure Databases for MySQL

Azure Database for MySQL has a fixed limit of allowed concurrent connections depending on the service tier and number of vCores that are provisioned for your server. The current max number of connections are published in our [documentation](https://docs.microsoft.com/azure/mysql/concepts-limits).

## **Recommended Steps**

* Review the [max connection limits](https://docs.microsoft.com/azure/mysql/concepts-limits) and scale your server to the right size to handle you load
* Investigate if all connections are actually used, or is some are idle. Closing idle connections and ideally using connection pooling help optimize the number of concurrent connections.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
