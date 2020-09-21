<properties
    pageTitle="Monitoring replication in Azure Database for MySQL Single Server"
    description="Monitoring replication in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="340"
    selfHelpType="generic"
    supportTopicIds="32747572"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbefb0c9-3e3e-4df9-b4f1-d12547cf58ef"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Monitoring replication in Azure Database for MySQL - Single Server

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* The *Replica lag* metric doesn't show any data: The **Replica Lag** metric is only applicable to replica servers. For each replica, this metric reflects the time since the last transaction that was replayed on that replica. The master server does not show data for this metric.
* The *Replica lag* metric is increasing: Confirm if the configuration of the replica server matches the master. For example, if you have increased the master's vCores, ensure the replica server's vCores are equal or greater than the master.

## **Recommended Documents**

* [How to monitor replication lag in the portal](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal#monitor-replication)
* [How to create and manage read replicas in the portal](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)