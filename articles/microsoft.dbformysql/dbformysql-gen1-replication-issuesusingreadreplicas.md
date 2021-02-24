<properties
    pageTitle="Issues using read replicas in Azure Database for MySQL Single Server"
    description="Issues using read replicas in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna,bahusse"
    displayOrder="330"
    selfHelpType="generic"
    supportTopicIds="32747568"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7d7ea843-9e29-4f1e-a7f7-f3cd0abeeba5"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues using read replicas in Azure Database for MySQL - Single Server

The read replica feature lets you replicate data from an Azure Database for MySQL Single Server to a read-only server. You can replicate up to five replicas from the master server. Replicas are updated asynchronously using the MySQL engine native binary log (`binlog`) file position-based replication technology.

Most users are able to resolve issues by using the steps below.

### **Fix it yourself**

**Troubleshooting replication lag?** 

Review [Common scenarios for high replication latency](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency#common-scenarios-for-high-replication-latency). Pay special attention to `binlog_group_commit_sync_delay` parameter, which controls how many microseconds the binary log commit waits before synchronizing the binary log file.


**Make sure all your tables have primary keys**

Lack of primary keys makes SQL thread scan all rows in the target table to apply the changes. This scan can cause replication latency.

**Note:** High resource usage (specifically IOPS, which are Intensive Write), causes multiplication of `binlog` files. Replaying these files on Read Replica slows down the overall replication performance and therefore might break replication.

Monitoring replication can be done through the **Replication lag in seconds** metric available on replica servers. This metric reflects the time since the last transaction was replayed on that replica and is calculated using the *seconds_behind_master* metric available in the MySQL engine. Alerts can be configured on this metric through Azure Monitor.

Learn how to [troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency).

**Replica creation is taking longer than expected**

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is due to the time it takes to restore all the data from your master server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.mysql.database.azure.com`.
2. If it's been at least five minutes since you requested the replica and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

**Replica creation fails using REST APIs, Azure Resource Manager, or Terraform, with "Unexpected error"**

If you are creating a read replica using REST APIs, ARM or Terraform, immediately after creation of the source server, the replica creation may fail with an "Unexpected error". This is because the initial backup of the source server, which is required to seed the read replica, may not be created yet. We recommend that you provision a read replica at least 15 minutes after creation of the source server to ensure initial backup is completed and available for replica seeding.

**Can't scale down replica's compute and storage**

The replica's compute and storage tiers should be equal or greater than the master server to ensure that the replica is able to keep up with the master server.

**Set up replica failover?**

You can choose to stop replication to a replica. Stopping replication disconnects the replica from the master server and makes the replica server a standalone read/write server.

Replicas do not automatically fail over. You have to choose to stop replication and redirect your application to point to the (former) replica's connection string. Make sure to also change the user name to include the correct server name after the @ sign. The replica will always have a unique connection string from the master server.

**Server parameters**

To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (for example, `log_bin_trust_function_creators` is locked on both master and replica). See the [documentation](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters) for the list of parameters that are locked.

To update one of the locked parameters on the master server: Delete replica servers, update the parameter value on the master, and re-create replicas.

**Move replicas to other subscriptions**

Replica servers are always created in the same resource group and same subscription as the master server. If you want to create a replica server in a different resource group or different subscription, you can [move the replica server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation.

### **Private link for replicas**

If you are using private link, make sure that you have a separate private link for replicas and ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)

## **Recommended Documents**

* [Troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency)
* [Read replica non-modifiable server parameters](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters)
