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
* The *Replica lag* metric is increasing: Confirm if the configuration of the replica server matches the source. For example, if you have increased the source server vCores, ensure the replica server's vCores are equal or greater than the.
* In Azure Database for MySQL, binary logging format is always **ROW**. If your table is missing primary key then all rows in the table is scanned for DML and this causes large amount of replication lag. To ensure that the replica is able to keep up with changes to the source, we generally recommend adding the primary key for the tables in master server before creating the replica server or re-creating the replica server if you already have one.

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)
* [How to monitor replication lag in single server](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal#monitor-replication)
* [How to create and manage read replicas in single server](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal)
* [Overview on read replicas in single server](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)
