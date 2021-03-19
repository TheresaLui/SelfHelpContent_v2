<properties
    pageTitle="General replication issues in Azure Database for PostgreSQL"
    description="Replication issues"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="420"
    selfHelpType="generic"
    supportTopicIds="32639992, 32780920"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="eda18367-7c0b-450c-a021-c35fe2b121d7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with replication

Most users are able to resolve their issues concerning replication by using the following information.

## **Recommended Steps**

**Replica server is writable, or has some other property expected only on primary server**

   * Connect to your replica server and run the following query: `SELECT pg_is_in_recovery();`. If this returns false, you are not connected to a replica server. Look at the username field (`username@servername`) in your connection string and confirm that the server name is the same as that of the replica.

**Replica lag is higher than usual**

   * Replica lag increase is typically caused by an increased load on the primary server. Consider reducing the load on the primary or [scaling up](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#scaling).
   * For most workloads, read replicas offer near-real-time updates from the primary. However, with persistent, heavy, write-intensive primary workloads, the replication lag can continue to grow and never catchup with the primary. This may also increase storage usage at the primary, because the WAL files are not deleted until they are received at the replica. If this situation persists, you can delete and re-create the read replica after the write-intensive workloads complete, to bring the replica back to a good state with respect to lag.
   * 
**Note:** Asynchronous read replicas are not suitable for such heavy write workloads. When evaluating read replicas for your application, monitor the lag on the replica for a full app work load cycle through its peak and non-peak times to access the possible lag and the expected RTO/RPO at various points of the workload cycle.

**Replica failover**

   * Replicas [do not automatically fail over](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#failover). You need to choose to stop replication and redirect your application to point to the (former) replica's connection string. The replica will always have a unique connection string from the primary server.

   * You can choose to stop replication to a replica. Stopping replication disconnects the replica from the primary server and makes the replica server a standalone read/write server.

**Query Performance Insight, Performance Recommendations, Query Store not working**

   * Replicas do not support Query Performance Insight and Performance Recommendation features. The Query Store database on replicas is a copy of the primary server's Query Store data.
   
   * After a replica becomes a standalone server, [set Query Store parameters](https://docs.microsoft.com/azure/postgresql/concepts-query-store#enabling-query-store) and restart the former replica to activate the feature.

**Can't scale down replica's compute**

   * The replica's compute should be equal to or greater than the primary server. [Learn more](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#scaling).

**Interested in logical replication**

   * Logical replication with Azure Database for PostgreSQL as a subscriber is not supported
   * Logical replication is a different PostgreSQL feature from [logical decoding](https://docs.microsoft.com/azure/postgresql/concepts-logical)

**Replica is not starting**

   * PostgreSQL requires the replica values of the `max_prepared_transactions`, `max_locks_per_transaction`, and `max_worker_processes` parameters be greater than or equal to the primary value; otherwise, the replica won't start. If you want to change one of these parameters on the primary, first change it on the replicas.

**Queries on the replica fail with error message "Canceling statement due to conflict with recovery. User query might have needed to see row versions that must be removed".**

   * Consider setting the parameter `hot_standby_feedback` to `ON`. To learn about this parameter, see [the PostgreSQL documentation](https://www.postgresql.org/docs/10/runtime-config-replication.html). [Learn how to set PostgreSQL server parameters in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal).

**Queries on the replica fail with error message "Canceling statement due to conflict with recovery. User was holding shared buffer pin for too long."**

   * Consider setting the parameters `max_standby_archive_delay` and `max_standby_streaming_delay` to a larger value. For an explanation of these parameters, see [PostgreSQL documentation](https://www.postgresql.org/docs/10/runtime-config-replication.html). [Learn how to set PostgreSQL server parameters in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal). 

## **Recommended Documents**

* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
* Learn about [logical decoding](https://docs.microsoft.com/azure/postgresql/concepts-logical)
