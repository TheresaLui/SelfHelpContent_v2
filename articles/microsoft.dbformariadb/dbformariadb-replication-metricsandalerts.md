<properties
    pageTitle="Monitoring replication in Azure Database for MariaDB"
    description="Metric issues"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="420"
    selfHelpType="generic"
    supportTopicIds="32673563"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4fcc0f1f-ce80-414d-bab3-33fb8303122d"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Monitoring replication

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* The *Replica lag* metric doesn't show any data: The **Replica Lag** metric is only applicable to replica servers. For each replica, this metric reflects the time since the last transaction that was replayed on that replica. The master server does not show data for this metric.
* The *Replica lag* metric is increasing: Confirm if the configuration of the replica server matches the master. For example, if you have increased the master's vCores, ensure the replica server's vCores are equal or greater than the master.

## **Recommended Documents**

* [How to monitor replication lag in the portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal#monitor-replication)<br>
* [How to create and manage read replicas in the portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal)<br>
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli)<br>
* [Overview on read replicas](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas)
