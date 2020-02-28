<properties
    pageTitle="Read replicas in Azure Database for MySQL"
    description="Support for read replica servers"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="370"
    selfHelpType="generic"
    supportTopicIds="32673559"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax"
    articleId="fde891c7-83d3-4ce3-bf27-10fcac81ce84"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Read replicas in Azure Database for MySQL

The read replica feature allows you to replicate data from an Azure Database for MySQL server to a read-only server. You can replicate from the master server to up to five replicas. Replicas are updated asynchronously using the MySQL engine's native binary log (binlog) file position-based replication technology.

## **Recommended Steps**

* **Issue**: Can't scale down replica's compute and storage

    * The replica's compute and storage tiers should be equal or greater than the master server to ensure the replica is able to keep up with the master server.

* **Issue**: Monitor replication lag

    *  The **Replica Lag** metric is available on replica servers to monitor the lag in seconds. This metric reflects the time since the last transaction that was replayed on that replica. The master server does not show data for this metric. Alerts can be configured on this metric through Azure Monitor.

## **Recommended Documents**

* Learn more about [read replica servers](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)
* Create and manage read replica servers using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal)
* Create and manage read replica servers using the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)
* [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/)
