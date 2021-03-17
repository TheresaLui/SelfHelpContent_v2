<properties
    pageTitle="Monitoring replication in Azure Database for MySQL Single Server"
    description="Monitoring replication in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna,bahusse"
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

Most users are able to resolve issues concerning monitoring replication in Azure Database for MySQL - Single Server by using the steps below.

#### **Fix it yourself**

**Troubleshooting replication lag?**

Review [Common scenarios for high replication latency](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency#common-scenarios-for-high-replication-latency). Pay special attention to the `binlog_group_commit_sync_delay` parameter, which controls how many microseconds the binary log commit waits before synchronizing the binary log file.

**Do all your tables have primary keys?** 

Azure Database for MySQL uses **ROW**-based binary logging. If your table is missing a primary key, all rows in the table are scanned for DML operations. This causes increased replication lag. To ensure that the replica is able to keep up with changes on the source, we recommend adding a primary key on tables in the source server before creating the replica server, or re-creating the replica server if you already have one.

**Note:** High resource usage (specifically, IOPS, which are Intensive Write) causes multiplication of `binlog` files. Replaying these files on Read Replica slows down the overall replication performance and might break replication.

Monitoring replication can be done through the **Replication lag in seconds** metric available on replica servers. This metric reflects the time since the last transaction that was replayed on that replica and is calculated using the *seconds_behind_master* metric available in the MySQL engine. Alerts can be configured on this metric through Azure Monitor.

**Replica lag metric doesn't show any data**

Replica Lag metric is only applicable to replica servers. For each replica, this metric reflects the time since the last transaction that was replayed on that replica. The master server does not show data for this metric.

**Replica lag metric is showing high replication lag** 

See [troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency).

**Replica lag metric is increasing** 

Confirm if the configuration of the replica server matches the master. For example, if you have increased the master's vCores, make sure that the replica server's vCores are equal or greater than the source.

## **Recommended Documents**

* [How to monitor replication lag in the portal](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal#monitor-replication)
* [Troubleshoot replication latency in Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/troubleshooting-replication-latency-in-azure-database-for-mysql/ba-p/1752473)
* [How to create and manage read replicas in the portal](https://docs.microsoft.com/azure/mysql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/mysql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)
