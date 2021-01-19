<properties
    pageTitle="Monitoring replication in Azure Database for MySQL"
    description="Monitoring replication in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="360"
    selfHelpType="generic"
    supportTopicIds="32640068"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ccea334d-5029-4671-beaa-55c0c3e21523"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Monitoring replication in Azure Database for MySQL

Azure Database for MySQL offers two deployment types - single server and flexible server. Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* The *Replication lag* metric doesn't show any data: The **Replication Lag** metric is only applicable to replica servers. For each replica, this metric reflects the time since the last transaction that was replayed on that replica. The source server does not show data for this metric.
* The *Replica Lag* metric is showing high replication lag: refer to [troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency).
* The *Replica lag* metric is increasing: Confirm if the configuration of the replica server matches the source. For example, if you have increased the source server vCores, ensure the replica server's vCores are equal or greater than the source.
* Azure Database for MySQL uses **ROW** based binary logging. If your table is missing a primary key, all rows in the table are scanned for DML operations. This causes increased replication lag. To ensure that the replica is able to keep up with changes on the source, we generally recommend adding a primary key on tables in the source server before creating the replica server or re-creating the replica server if you already have one.

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)
* [Troubleshoot replication latency in Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/troubleshooting-replication-latency-in-azure-database-for-mysql/ba-p/1752473)
* [How to monitor replication lag in single server](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal#monitor-replication)
* [How to create and manage read replicas in single server](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal)
* [Overview on read replicas in single server](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)
