<properties
    pageTitle="Issues using replicas in Azure Database for MySQL"
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
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fde891c7-83d3-4ce3-bf27-10fcac81ce84"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues using read replicas in Azure Database for MySQL

The read replica feature lets you replicate data from an Azure Database for MySQL to a read-only server. You can replicate from the source server to up to five replicas in Azure Database for MySQL- Single Server and up to 10 replicas Azure Database for MySQL- Flexible Server. Replicas are updated asynchronously using the MySQL engine's native binary log (`binlog`) file position-based replication technology.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

### Large amount of replication lag

Monitoring replication can be done through the **Replication lag in seconds** metric available on replica servers. This metric reflects the time since the last transaction that was replayed on that replica and is calculated using the **seconds_behind_master** metric available in the MySQL engine. Alerts can be configured on this metric through Azure Monitor.

Refer to [troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency) to learn on how to troubleshoot replication latency.

### **Replica creation is taking longer than expected**

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.mysql.database.azure.com`.
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

### **Replica creation failing using REST APIs, Azure Resource Manager or Terraform fails with Unexpected error**

If you are creating a read replica using REST APIs, ARM or Terraform,  immediately after creation of the source server, the replica creation may fail with "Unexpected error". This is because the initial backup of the source server which is required to seed the read replica may not be created yet. We recommend that you provision a read replica at least 15 minutes after creation of the source server to ensure that the initial backup is completed and available for replica seeding.

### **Can't scale down replica's compute and storage**

The replica's compute and storage tiers should be equal or greater than the master server to ensure the replica is able to keep up with the master server.

### **Replica failover**

You can choose to stop replication to a replica. Stopping replication disconnects the replica from the master server and makes the replica server a standalone read/write server.

Replicas do not automatically failover. You have to choose to stop replication and redirect your application to point to the (former) replica's connection string. Make sure to also change the user name to include the correct server name after the @ sign. The replica will always have a unique connection string from the master server.

### **Server parameters**

To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (for example, `log_bin_trust_function_creators` is locked on both master and replica). Refer to the [documentation](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters) for the list of locked parameters.

To update one of the locked parameters on the master server, delete replica servers, update the parameter value on the master, and re-create replicas.

### **Move replicas to other subscriptions**

Replica servers are always created in the same resource group and same subscription as the master server. If you want to create a replica server in a different resource group or different subscription, you can [move the replica server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation.

### **Private link for replicas in Azure Database for MySQL- Single Server**

If you are using private link, make sure that you have a separate private link for replicas and ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal).

## **Recommended Documents**

* [Troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency)
* [Read replica non-modificable server parameters](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#server-parameters)
