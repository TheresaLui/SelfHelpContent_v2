<properties
    pageTitle="Monitoring replication in Azure Database for PostgreSQL"
    description="Metric issues"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="430"
    selfHelpType="generic"
    supportTopicIds="32639995, 32780921"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fba936eb-4442-45b7-b086-a4b6b912d5ac"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Monitoring replication

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

Issue: What is the **RTO, RPO** for replicas?
   * Read replicas do not have a guaranteed RTO, RPO
   * In most cases, replica lag ranges between a few seconds to a couple minutes. You can track your actual replication lag using the metric *Replica Lag*. Learn more about the [replica lag metric](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#monitor-replication).
   * Once you initiate [stop replication](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas#stop-replication), the backend process typically takes about 2 minutes to complete

Issue: **Query Performance Insight**, Performance Recommendations, Query Store not working on replica

   * Replicas do not support Query Performance Insight and Performance Recommendation features. The Query Store database on replicas is a copy of the master server's Query Store data. 


Issue: The ***Replica lag* metric doesn't show any data**.

   * The **Replica Lag** metric is only applicable to replica servers. For each replica, this metric reflects the time since the last transaction that was replayed on that replica. The master server does not show data for this metric.

For the master server, we provide a *Max lag across replicas* metric.

Issue: The ***Max lag across replicas* metric doesn't show any data**.

   * The *Max lag across replicas* metric is only applicable to the master server. This metric shows the lag in bytes between the master and its most lagging replica. Replica servers do not show data for this metric.

   * For replica servers we provide a *Replica lag* metric.

Issue: The ***Replica lag* metric shows a lag** of up to 5 minutes even when there is no load on the master and the replica is up to date.

   * The *Replica lag* metric is calculated as:

   ```SQL
   SELECT EXTRACT(EPOCH FROM now() - pg_last_xact_replay_timestamp());
   ```

   The replica lag metric indicates the last time since a log record from the master was applied to this replica. When there is no load on the master, this metric value continues to increase.

   Periodically, an agent does a check on the master and on the replica. If you don't have any load on your master server, you will see this check reflected in the *Replica lag* metric as a ceiling between 3 to 5 minutes. 

**Issue:** The *Max lag across replicas* value is increasing continuously.

   * If *Max lag across replicas* is continuously increasing, it may be because streaming replication is interrupted between the servers. To check if streaming replication is interrupted, connect to the master and run the following query:

   ```
   SQL
   SELECT application_name, active FROM pg_replication_slots AS slots LEFT JOIN pg_stat_replication AS stats ON stats.pid = slots.active_pid;
   ```

   The *application_name* column provides the replica names. The *active* column indicates the status of replication. If one of the values of *active* is false, streaming replication is inactive between the master and that replica. This may be because the replica or master recently experienced a restart. In that case, streaming replication should resume shortly. 

   * If *active* is true for all replicas, then it is likely that there is high write activity on the master. The replicas will eventually catch up once load on the master reduces. If you see that a replica is regularly lagging after a master, consider scaling up the replica so it can replay data faster.

Issue: ***Max lag across replicas* always shows as 0**.

   * The *Max lag across replicas* metric shows the lag in bytes between the master and its most lagging replica. If all replicas are up to date with the master, the value will be 0.

   * If data is missing from your replica while *Max lag across replicas* continues to be 0, proceed to open a support ticket. 

Issue: **Receiving a number of alerts with  *max lag exceeding number of bytes***

 Please check your alert setting for maximum replica lag metric. It may be too low (may be in KBs) for your workload. Depending in your workload and the replica placement, the replica may be hitting this alert limit often. In such case, please consider increasing the max replica lag limit to a higher value - to even in MBs.

## **Recommended Documents**

* [How to create and manage read replicas in the portal](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-portal)
* [Use Azure CLI to create and manage read replicas](https://docs.microsoft.com/azure/postgresql/howto-read-replicas-cli)
* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
