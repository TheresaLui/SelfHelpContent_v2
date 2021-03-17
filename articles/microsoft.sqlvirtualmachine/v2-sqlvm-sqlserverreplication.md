<properties
  pagetitle="Always On, High Availability, Disaster Recovery - SQL Server Replication"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740093"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="1e3613d5-cd3e-4a00-ba62-f84def317cab"
  ownershipid="AzureData_AzureSQLVM" />
# Always On, High Availability, Disaster Recovery - SQL Server Replication


4 out of 5 customers are able to resolve their SQL Server Replication issues using the following steps.

## **Recommended Steps**


* **Common Solutions for Replication** 

  * You can easily configure **[Replication with Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-replication-for-always-on-availability-groups-sql-server?view=sql-server-2017)**. Secondary Read Only Always On Replica cannot act as a Publisher until you have failed this over and made the primary replica.

   * **If you are having issues with permissions**, verify the accounts under which agents run and make connections have [Correct Permissions](https://docs.microsoft.com/sql/relational-databases/replication/security/replication-agent-security-model?view=sql-server-ver15#permissions-that-are-required-by-agents)

  *  You may have **connectivity issues** when setting up Replication. Make sure you can telnet to the distributor or subscriber. Please verify Windows Firewall and Network Security Groups are not blocking the connections. If you are using [Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/replication-to-sql-database), Ensure that the port ranges of 11000-11999 on your Azure client machine are available for communication.

  * Review **Common Errors** with Replication and [additional information](https://docs.microsoft.com/sql/relational-databases/replication/errors-and-events-reference-replication?view=sql-server-ver15)

   * If you cannot configure Replication using SSMS between various SQL versions, [Configure Replication using T-SQL](https://docs.microsoft.com/sql/relational-databases/replication/configure-publishing-and-distribution?view=sql-server-ver15#TsqlProcedure)

   * Migrate your Replication from SQL 2012 to any new SQL Versions using [Backup or Restore Database](https://docs.microsoft.com/sql/relational-databases/tutorial-sql-server-backup-and-restore-to-azure-blob-storage-service?view=sql-server-ver15&tabs=SSMS)

   * Most Replication issues can be fixed by **Rebuilding the publication/subscription**, by deleting a [Pull](https://docs.microsoft.com/sql/relational-databases/replication/delete-a-pull-subscription?view=sql-server-ver15) or [Push](https://docs.microsoft.com/sql/relational-databases/replication/delete-a-push-subscription?redirectedfrom=MSDN&view=sql-server-ver15) Subscription, [Deleting a Publication](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms147833(v=sql.105)?redirectedfrom=MSDN) and Disabling [Publishing and Distribution](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms151181(v=sql.105)?redirectedfrom=MSDN) and [Setting it up again](https://docs.microsoft.com/sql/relational-databases/replication/tutorial-preparing-the-server-for-replication?view=sql-server-ver15)
 
   * You can add or delete articles regarding Replication and Synchronization by following [these guidelines](https://docs.microsoft.com/sql/relational-databases/replication/publish/add-articles-to-and-drop-articles-from-existing-publications?view=sql-server-ver15)

 * **Error: "Replicated transactions are waiting for next Log backup or for mirroring partner to catch up"**

   * This can happen if you have set up replication to [Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/replication-to-sql-database). Performing a log backup will resolve this problem.
    * This can also happen if you configured replication with Always on Adding [Trace Flag 1448](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-traceon-trace-flags-transact-sql?redirectedfrom=MSDN&view=sql-server-ver15), which allows the log reader to do the log scan on replication without a SQL restart


* **Improving Performance and Troubleshooting Latency Issues with Transactional Replication**

   * In Azure VM, [Throttling and Throughput](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics) issues on your server can cause slowdown and create latency. If you are getting VM-level throttling, upsizing the VM can help.

   * [Use Tracer Token](https://docs.microsoft.com/sql/relational-databases/replication/monitor/measure-latency-and-validate-connections-for-transactional-replication?view=sql-server-ver15#to-insert-a-tracer-token-and-view-information-on-the-token) to measure if latency is from publisher to Distributor, Distributor to Subscriber or to calculate the total Latency.

   * Make sure you do run your transaction in batches instead of a single large transaction.

   * Tune your [Distribution Agent and Log Reader Agent Parameters](https://docs.microsoft.com/sql/relational-databases/replication/administration/enhance-transactional-replication-performance?view=sql-server-ver15#distribution-agent-and-log-reader-agent-parameters)

   * Enhance your transactional [Replication Performance](https://docs.microsoft.com/sql/relational-databases/replication/administration/enhance-transactional-replication-performance?view=sql-server-ver15) 


## **Recommended Documents**
* [Replication Setup Tutorials](https://docs.microsoft.com/sql/relational-databases/replication/replication-tutorials?view=sql-server-ver15)
* [Enhance replication performance](https://docs.microsoft.com/sql/relational-databases/replication/administration/enhance-general-replication-performance)
* [Best practices for replication administration](https://docs.microsoft.com/sql/relational-databases/replication/administration/best-practices-for-replication-administration)
* [FAQ for replication administrators](https://docs.microsoft.com/sql/relational-databases/replication/administration/frequently-asked-questions-for-replication-administrators)
* [Configuring replication distribution database in Always On AG](https://docs.microsoft.com/sql/relational-databases/replication/configure-distribution-availability-group)
* [Troubleshoot error 20598 - The row was not found at the Subscriber](https://support.microsoft.com/help/3066750/how-to-troubleshoot-error-20598-the-row-was-not-found-at-the-subscribe)
