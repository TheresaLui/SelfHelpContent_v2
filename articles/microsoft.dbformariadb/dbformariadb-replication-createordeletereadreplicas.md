<properties
    pageTitle="Create and delete read replicas in Azure Database for Mariadb"
    description="Create and delete read replicas"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="350"
    selfHelpType="generic"
    supportTopicIds="32688608"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax"
    articleId="fa0d8532-80d8-4dc8-98d8-d7dfdf0ef921"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Create and delete read replicas

The read replica feature allows you to replicate data from an Azure Database for Mariadb server to a read-only server. You can replicate from the master server to up to five replicas. Replicas are updated asynchronously using the MariaDB engine's native binary log (binlog) file position-based replication technology.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

### **Replica creation is taking longer than expected**

Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.mariadb.database.azure.com`.
2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

### **Replica failover**

You can choose to stop replication to a replica. Stopping replication disconnects the replica from the master server and makes the replica server a standalone read/write server.

Replicas do not automatically failover. You have to choose to stop replication and redirect your application to point to the (former) replica's connection string. Make sure to also change the user name to include the correct server name after the @ sign. The replica will always have a unique connection string from the master server.

### **Deleting replica servers**

Replica servers can be deleted from the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal#delete-a-replica-server) or [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli#delete-a-replica-server).

### **Deleting master servers**

Master servers can be deleted from the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal#delete-a-master-server) or [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli#delete-a-master-server).

Deleting a master server stops replication to all replica servers and deletes the master server itself. Replica servers become standalone servers that now support both read and writes.

### **Server parameters**

To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas. Refer to [documentation](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#server-parameters) for the list of parameters that are locked.

## **Recommended Documents**

* [Create and manage read replicas in the portal](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/mariadb/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas)