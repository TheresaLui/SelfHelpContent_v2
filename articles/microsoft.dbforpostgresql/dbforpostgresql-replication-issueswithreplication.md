<properties
    pageTitle="General replication issues in Azure Database for PostgreSQL"
    description="Replication issues"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="420"
    selfHelpType="generic"
    supportTopicIds="32639992"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="eda18367-7c0b-450c-a021-c35fe2b121d7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Issues with replication

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

Issue: **Replica server is writable**, or has some other property expected only on master

Connect to your replica server and run the following query: `SELECT pg_is_in_recovery();`. If this returns false, you are not connected to a replica server. Look at the username field (username@servername) in your connection string. Confirm that the server name is the same as that of the replica.

Issue: **Replica is not starting**

PostgreSQL requires the replica values of the max_prepared_transactions, max_locks_per_transaction, and max_worker_processes parameters be greater than or equal to the master value; otherwise, the replica won't start. If you want to change one of these parameters on the master, first change it on the replicas.

Issue: **Replica failover**

You can choose to stop replication to a replica. Stopping replication disconnects the replica from the master server and makes the replica server a standalone read/write server.

Replicas [do not automatically failover](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#failover). You have to choose to stop replication and redirect your application to point to the (former) replica's connection string. The replica will always have a unique connection string from the master server.

Issue: **Query Performance Insight**, Performance Recommendations, Query Store not working on replica

Replicas do not support Query Performance Insight and Performance Recommendation features. The Query Store database on replicas is a copy of the master server's Query Store data. 

Issue: **Can't scale down** replica's compute and storage

The replica's compute and storage tiers should be equal or greater than the master server to ensure the replica is able to keep up with the master server.

Issue: **Queries on the replica fail** with error message "Canceling statement due to conflict with recovery. **User query might have needed to see row versions that must be removed**."

Consider setting the parameter `hot_standby_feedback` to `ON`. To learn about this parameter, see [the PostgreSQL documentation](https://www.postgresql.org/docs/10/runtime-config-replication.html). [Learn how to set PostgreSQL server parameters in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal).


Issue: **Queries on the replica fail** with error message "Canceling statement due to conflict with recovery. **User was holding shared buffer pin for too long**."

Consider setting the parameters `max_standby_archive_delay` and `max_standby_streaming_delay` to a larger value. For an explanation of these parameters see [the PostgreSQL documentation](https://www.postgresql.org/docs/10/runtime-config-replication.html). [Learn how to set PostgreSQL server parameters in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal). 

## **Recommended Documents**

* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
