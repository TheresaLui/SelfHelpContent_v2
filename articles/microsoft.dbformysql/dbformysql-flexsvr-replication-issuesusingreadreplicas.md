<properties
    pageTitle="Issues using read replicas in Azure Database for MySQL - Flexible Server"
    description="Issues using read replicas in Azure Database for MySQL - Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="320"
    selfHelpType="generic"
    supportTopicIds="32747621"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="51662208-c1ea-4396-8491-ab39c8f57cf5"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues using read replicas in Azure Database for MySQL - Flexible Server

The read replica feature allows you to replicate data from an Azure Database for MySQL Flexible Server to a read-only server. You can replicate from the source server to up to five replicas. Replicas are updated asynchronously using the MySQL engine's native binary log (binlog) file position-based replication technology.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

### Large amount of replication lag

Azure Database for MySQL uses **ROW** based binary logging. If your table is missing a primary key, all rows in the table are scanned for DML operations. This causes increased replication lag. To ensure that the replica is able to keep up with changes on the source, we generally recommend adding a primary key on tables in the source server before creating the replica server or re-creating the replica server if you already have one.

Refer to [troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency) to learn on how to troubleshoot replication latency.

### **Replica creation is taking longer than expected**

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your source server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.mysql.database.azure.com`.
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

### **Can't scale down replica's compute and storage**

You can scale replica's compute tier after creating the replica. The storage tier should be equal or greater than the source server. we recommend to keep the compute size of replica to be equal or greater than the source server to ensure the replica is able to keep up with the source server.

### **Replica failover**

You can choose to stop replication to a replica. Stopping replication disconnects the replica from the source server and makes the replica server a standalone read/write server.

Replicas do not automatically failover. You have to choose to stop replication and redirect your application to point to the (former) replica's connection string. The replica will always have a unique connection string from the source server.

### **Deleting replica servers**

Replica servers can be deleted from the Azure portal or Azure CLI.

### **Deleting source servers**

Source servers can be deleted from the Azure portal or Azure CLI.

Deleting a source server stops replication to all replica servers and deletes the source server itself. Replica servers become standalone servers that now support both read and writes.

### **Server parameters**

To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (ex. `log_bin_trust_function_creators` is locked on both source and replica).

To update one of the locked parameters on the source server, please delete replica servers, update the parameter value on the source, and recreate replicas.

### **Replication lag**

Monitoring replication can be done through the **Replication lag in seconds** metric available on replica servers. This metric reflects the time since the last transaction that was replayed on that replica and is calculated using the *seconds_behind_master* metric available in the MySQL engine. Alerts can be configured on this metric through Azure Monitor.

### **Move replicas to other subscriptions**

Replica servers are always created in the same resource group and same subscription as the source server. If you want to create a replica server in a different resource group or different subscription, you can [move the replica server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation.

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)
* [Troubleshoot replication latency in Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/troubleshooting-replication-latency-in-azure-database-for-mysql/ba-p/1752473)
* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)