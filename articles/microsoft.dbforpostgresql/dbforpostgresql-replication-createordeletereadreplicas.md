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

Most users are able to resolve their issue using the steps below.

## Creating read replica: Frequently asked questions

* **How do I add a read replica to my server?** <br>
  You can add up to 5 read replicas across regions using portal or CLI. Note that you cannot choose a different compute/storage tier for your replica. The replica server will be provisioned with similar resource like your primary server.

* **Can read replicas be configured in synchronous mode?** <br>
  No. Only asynchronous mode of replication is supported. This helps with non-impact for application writes and commits at the primary site.

* **What technology you use for replica?** <br>
  PostgreSQL's native WAL streaming replication is used.

* **What use cases read replicas server?** <br>
  Read replicas servers two purposes.
  1. Offload read queries to read replica so that your primary server can serve write requests more efficiently.
  2. Helps with disaster recovery where in the event of primary server unavailable, you can failover to the read replica.
   
* **While creating new replica, why my preferred region not listed?** <br>
  The list of available cross-regions depends on your master server's region. Visit the [read replica documentation for more information](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#cross-region-replication). We are working to expand to more regions in the future.

* **How do I connect to the replica server?** <br>
  Replica server is a physically separate server with its own end point (host). You can connect to the replica server using its end point and using `username@replica-server-name` user name.

* **How do I find the replica lag?** <br>
   You can monitor replica lag and maximum replica lag across many replicas in the portal. You can even set alerts if the lag exceeds certain threshold - for example > 10 minutes.

* **Why i am seeing excessive replica lag?** <br>
  In many cases, the source server may be doing heavy write-intensive workload which needs to be transmitted to the remote region. PostgreSQL's apply of WAL at the replica is usually single-threaded. This may introduce the lag.

* **What do I do if the replica lag is in hours - though my server is small in size (few GBs)?** <br>
  In such cases, it is faster to just drop the replica server and recreate a fresh replica server.

* **Why *Add Replica* button is disabled?** <br>

  1. Refresh the *Replication* portal page
  2. Confirm that you've selected *replica* or *logical* for your replication support level. [Learn more about these settings](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#prerequisites).
  3. Restart the server

* **Why my replica creation is taking longer than expected?** <br>

    Depending on the size of the server, replica creation time can vary from a few minutes to a few hours. This is because of the time it takes to restore all the data from your master server to the replica.

  1. Using Azure Cloud Shell, ping the DNS of the replica. For example, if you named the replica `myreplica`, the DNS name is `myreplica.postgres.database.azure.com`.
  2. If it's been at least five minutes since you requested the replica, and the name is resolving, then replica creation is in progress. If the name is not resolving, proceed to open a support ticket.

## Failover/Stop Replica: Frequently asked questions

* **Is the failover to the replica automatic?** <br>
  No. You have to manually trigger the failover. This is because, the replication happens in asynchronous mode which might incur data loss. Hence we do not want to automatically failover.

* **How do I trigger a failover?** <br>
  From the portal, from "Replication" blade, you click the replica that you want to failover to. Then click `Stop Replication` button. This will stop the replication and also promotes the read replica to be a standalone, read-writeable independent server. You can connect to that server for your read and write operations. 

  If you prefer CLI, you can run `az postgres server replica stop -g <resourceGroup> -n <replServer>` command.

  Note: Once the connection between the primary and the replica is severed, you cannot re-attach the replica. You would have to create a new replica server.

* **Can I use the same hostname (end point) for the replica server after the failover?** <br>
  The replica server is a different server with a different end point. If you want to use the same name, then you may choose to deploy a proxy such as pgbouncer, pgpool-II, or third party proxy to point the same endpoint to point to the replica server name.

* **How do I setup a new replica for the failed over server?** <br>
   The process is same as creating a new replica in your preferred region.

* **How do I failback to the old primary?** <br>
  Failback feature is not available with the service. If you have failed over server-A from region-A to the replica in region-B, then 
  1. You have to create a new replica server-A2 (different name) in region-A. 
  2. After the replication creation, you can perform another failover (stop replica) which makes server-A2 independent.
  3. You can then start using server-A2 for production and optionally create a replica in another region for DR.
  4. If you want to use the same name server-A in the failback scenario, you would have to first delete the original server-A before step #1.
 

## **Recommended Documents**

* [Restart your server](https://docs.microsoft.com/azure/postgresql/howto-restart-server-portal)
* [Create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
