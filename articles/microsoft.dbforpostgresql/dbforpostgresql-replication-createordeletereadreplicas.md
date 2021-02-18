<properties
    pageTitle="Create read replicas in Azure Database for PostgreSQL"
    description="Create replicas"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="410"
    selfHelpType="generic"
    supportTopicIds="32639973, 32780918"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9e065390-0a87-42d8-812b-39f24f7d04c7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Creating and deleting read replicas

Most users are able to resolve issues they experience when creating and deleting read replicas by using the following information.

## Creating read replica: Frequently asked questions

* **How do I add a read replica to my server?** <br>
  You can add up to 5 read replicas across regions using Azure portal or CLI. Note that you cannot choose a different compute/storage tier for your replica. The replica server will be provisioned with similar resources, like your primary server.

* **Can read replicas be configured in synchronous mode?** <br>
  No. Only asynchronous mode of replication is supported. This helps with non-impact for application writes and commits at the primary site.

* **What technology you use for replica?** <br>
  We use the PostgreSQL native WAL streaming replication.

* **What use cases involve read replicas server?** <br>
  Read replicas servers serve two purposes.
  1. Offload read queries to read replica so that your primary server can serve write requests more efficiently.
  2. Help with disaster recovery where, if the primary server unavailable, you can fail over to the read replica.
   
* **While creating new replica, why is my preferred region not listed?** <br>
  The list of available cross-regions depends on your master server's region. For more information, see the [read replica documentation](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#cross-region-replication). We are working to expand to more regions in the future.

* **How do I connect to the replica server?** <br>
  The replica server is a physically separate server with its own end point (host). You can connect to the replica server using its end point and using the `username@replica-server-name` user name.

* **How do I find the replica lag?** <br>
   You can monitor replica lag and maximum replica lag across many replicas in Azure portal. You can even set alerts if the lag exceeds certain threshold; for example, > 10 minutes.

* **Why am I seeing excessive replica lag?** <br>
  In many cases, the source server is performing a heavy, write-intensive workload that needs to be transmitted to the remote region. PostgreSQL's apply of WAL at the replica is usually single-threaded. This can introduce the lag.

* **What do I do if the replica lag is in hours, although my server is small in size (few GBs)?** <br>
  In such cases, it is faster to just drop the replica server and re-create a fresh replica server.

* **Why is the Add Replica button disabled?** <br>
  1. Refresh the Replication portal page
  2. Confirm that you've selected **replica** or **logical** for your replication support level. [Learn more about these settings](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#prerequisites).
  3. Restart the server

* **Why is my replica creation taking longer than expected?** <br>
    Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

  1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.postgres.database.azure.com`.
  2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

## Failover/Stop Replica: Frequently asked questions

* **Is the failover to the replica automatic?** <br>
  No. You have to manually trigger the failover. This is because the replication happens in asynchronous mode, which might incur data loss. Therefore, we do not want to automatically failover.

* **How do I trigger a failover?** <br>
  From Azure portal, in the **Replication** blade, select the replica that you want to fail over to. Then select the **Stop Replication** button. This will stop the replication and also promote the read replica to be a standalone, read-writeable independent server. You can connect to that server for your read and write operations. 

  If you prefer CLI, you can run `az postgres server replica stop -g <resourceGroup> -n <replServer>` command.

  **Note:** After the connection between the primary and the replica is severed, you cannot re-attach the replica. You need to create a new replica server.

* **Can I use the same hostname (end point) for the replica server after the failover?** <br>
  The replica server is a different server with a different end point. If you want to use the same name, then you may choose to deploy a proxy such as `pgbouncer`, `pgpool-II`, or a third-party proxy to point the same endpoint to point to the replica server name.

* **How do I set up a new replica for the failed over server?** <br>
   The process is same as creating a new replica in your preferred region.

* **How do I fail back to the old primary?** <br>
  The failback feature is not available with the service. If you have failed over server-A from region-A to the replica in region-B, then: 
  1. You need to create a new replica server-A2 (different name) in region-A. 
  2. After the replica is created, you can perform another failover (stop replica), which makes server-A2 independent.
  3. You can then start using server-A2 for production, and optionally create a replica in another region for DR.
  4. If you want to use the same name server-A in the failback scenario, you first need to delete the original server-A before step #1.

## **Recommended Documents**

* [Restart your server](https://docs.microsoft.com/azure/postgresql/howto-restart-server-portal)
* [Create and manage read replicas in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
* [Overview about read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
