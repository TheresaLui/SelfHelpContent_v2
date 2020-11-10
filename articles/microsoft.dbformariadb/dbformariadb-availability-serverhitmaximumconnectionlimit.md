<properties
    pageTitle="Connection issues to MariaDB"
    description="Connection issues to MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="10"
    selfHelpType="generic"
    supportTopicIds="32640152"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="77831781-a014-4c00-a0a2-d366353a844d"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Connection issues to Azure Databases for MariaDB

Azure Database for MariaDB has a fixed limit of allowed concurrent connections depending on the service tier and number of vCores that are provisioned for your server. The current max number of connections are published in our [documentation](https://docs.microsoft.com/azure/mariadb/concepts-limits).

## **Recommended Steps**

* Review the [max connection limits](https://docs.microsoft.com/azure/mariadb/concepts-limits) and scale your server to the right size to handle you load
* Investigate if all connections are actually used, or is some are idle. Closing idle connections and ideally using connection pooling help optimize the number of concurrent connections.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)
