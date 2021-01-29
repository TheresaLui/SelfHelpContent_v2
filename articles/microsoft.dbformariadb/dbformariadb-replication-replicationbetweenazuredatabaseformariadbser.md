<properties
    pageTitle="Issues using read replicas in Azure Database for MariaDB"
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

# Issues using read replicas in Azure Database for MariaDB

The read replica feature allows you to replicate data from an Azure Database for MariaDB server to a read-only server. You can replicate from the master server to up to five replicas. Replicas are updated asynchronously using the MariaDB engine's native binary log (binlog) file position-based replication technology.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

### **Replica creation is taking longer than expected**

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.mariadb.database.azure.com`.
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

### **Can't scale down replica's compute and storage**

The replica's compute and storage tiers should be equal or greater than the master server to ensure the replica is able to keep up with the master server.

### **Replica failover**

You can choose to stop replication to a replica. Stopping replication disconnects the replica from the master server and makes the replica server a standalone read/write server.

Replicas do not automatically failover. You have to choose to stop replication and redirect your application to point to the (former) replica's connection string. Make sure to also change the user name to include the correct server name after the @ sign. The replica will always have a unique connection string from the master server.

### **Deleting replica servers**

Replica servers can be deleted from the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal#delete-a-replica-server) or [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli#delete-a-replica-server).

### **Deleting master servers**

Master servers can be deleted from the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal#delete-a-master-server) or [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli#delete-a-master-server).

Deleting a master server stops replication to all replica servers and deletes the master server itself. Replica servers become standalone servers that now support both read and writes.

### **Server parameters**

To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (ex. `log_bin_trust_function_creators` is locked on both master and replica). Refer to [documentation](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#server-parameters) for the list of parameters that are locked.

To update one of the locked parameters on the master server, please delete replica servers, update the parameter value on the master, and recreate replicas.

### **Replication lag**

Monitoring replication can be done through the **Replication lag in seconds** metric available on replica servers. This metric reflects the time since the last transaction that was replayed on that replica and is calculated using the *seconds_behind_master* metric available in the MariaDB engine. Alerts can be configured on this metric through Azure Monitor.

### **Move replicas to other subscriptions**

Replica servers are always created in the same resource group and same subscription as the master server. If you want to create a replica server in a different resource group or different subscription, you can [move the replica server](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) after creation.

## **Recommended Documents**

* Learn more about [read replica servers](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas)
* Create and manage read replica servers using the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal)
* Create and manage read replica servers using the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli)
* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/)