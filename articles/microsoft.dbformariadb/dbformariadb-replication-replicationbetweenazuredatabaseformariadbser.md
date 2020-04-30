<properties
    pageTitle="Read replicas in Azure Database for MariaDB"
    description="Support for read replica servers"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="370"
    selfHelpType="generic"
    supportTopicIds="32688607"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="afd5a2b3-7da5-4372-9e06-f4d8d3633b93"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Read replicas in Azure Database for MariaDB

The read replica feature allows you to replicate data from an Azure Database for MariaDB server to a read-only server. You can replicate from the master server to up to five replicas. Replicas are updated asynchronously using the MariaDB engine's native binary log (binlog) file position-based replication technology.

## **Recommended Steps**

* **Issue**: Can't scale down replica's compute and storage

    * The replica's compute and storage tiers should be equal or greater than the master server to ensure the replica is able to keep up with the master server.

* **Issue**: Monitor replication lag

    *  The **Replica Lag** metric is available on replica servers to monitor the lag in seconds. This metric reflects the time since the last transaction that was replayed on that replica. The master server does not show data for this metric. Alerts can be configured on this metric through Azure Monitor.

## **Recommended Documents**

* Learn more about [read replica servers](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas)
* Create and manage read replica servers using the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal)
* Create and manage read replica servers using the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli)
* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/)
