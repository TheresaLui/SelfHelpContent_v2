<properties
  pagetitle="Troubleshooting unexpected increase in resource consumption"
  description="Troubleshooting unexpected increase in resource consumption"
  service="microsoft.dbforpostgresql"
  resource="servers"
  ms.author="sunila,abkumbha"
  selfhelptype="Generic"
  supporttopicids="32640027,32781016"
  resourcetags="servers,databases"
  productpesids="16222,17067"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="3f47468a-cc1e-41c2-9665-57b66bbe16e2"
  ownershipid="AzureData_AzureDatabaseforPostgreSQL" />
# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload. Increased CPU usage can also be caused by an issue with PostgreSQL internal processes, such as autovacuum not running as expected, or an unexpected increase in short-lived connections. For example, if you open large number of connections at the same time, you will see performance slowdown.

 **Fix it yourself**

**Troubleshoot CPU high utilization?**
Review the [Performance Recommendations - Azure Database for PostgreSQL - Single Server |       Microsoft Docs](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations?WT.mc_id=Portal-Microsoft_Azure_Support). Please leverage [Query Store](https://docs.microsoft.com/azure/postgresql/concepts-query-store#:~:text=Enable%20Query%20Store%20using%20the%20Azure%20portal%201,4%20Set%20the%20value%20to%20TOP%20and%20Save.) to determine which queries are taking longest. If after optimizing the long running queries CPU usage is still high, consider scaling up to the next vCore tier. For example, if the CPU usage is hovering around 100 percent consistently for General Purpose 4 vCore, scale up to a General Purpose 8 vCore. High CPU usage is not the only indicator of CPU bottleneck. Single-threaded applications can also result in CPU exhaustion of one CPU while the other CPUs are under-utilized. Consider parallelizing your workload to take advantage of all the vCores available. [How Parallel Query Works?](https://www.postgresql.org/docs/current/how-parallel-query-works.html)

**Consider connection pooling**
Opening a new PostgreSQL connection is an expensive operation in terms of CPU used. The first is that we have a central gateway that allows us to provide built in high availability. You can see more about this architecture at [https://docs.Microsoft.com/azure/Postgresql/concepts-connectivity-architecture](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture). The second, is that because we ensure everything is encrypted in transit Postgres has to do an initial TLS negotiation. This is a recommended practice anytime running within the cloud. The combination of these two items means the cost of establishing a connection is often expensive. To reduce the time and cost of establishing an initial connection we recommend using a connection pooler.
[Connection handling best practices.](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/connection-handling-best-practice-with-postgresql/ba-p/790883)
[Steps to install PgBouncer connection pooling proxy.](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/steps-to-install-and-setup-pgbouncer-connection-pooling-proxy/ba-p/730555)

**Check for excessive logging**
Excessive logging can cause high resource utilization and slow down the system. With certain configurations, your PostgreSQL database server outputs a high amount of log lines. We recommend that you test with the following log configuration settings, and then verify whether this improves resource utilization.
* log_duration = OFF
* log_min_duration_statement = -1
* log_statement_stats = OFF
* log_statement = NONE
* pg_stat_statements.track = NONE

**Azure DB for PostgreSQL runs slower than usual**
When a database table is suffering from bloat, query performance will suffer dramatically. This can also increase the Resource consumption of the server. Please consider reviewing [Optimize autovacuum on Azure Database for PostgreSQL - Single Server.](https://docs.microsoft.com/azure/postgresql/howto-optimize-autovacuum?WT.mc_id=Portal-Microsoft_Azure_Support) Analyzing your tables frequently pushes better execution plans for your queries. PostgreSQL is a smart database engine, it’s probably best to let PostgreSQL do the vacuuming and analyzing rather than doing those manually.

**Are you using Basic Tier server?**
Basic tier servers are intended for testing, development, or small-scale infrequently used applications. A production workload can max out resources easily. For more information read [Understanding Performance in Basic Tier for Azure Database PostgreSQL.](https://techcommunity.microsoft.com/t5/azure-database-support-blog/understanding-performance-in-basic-tier-for-azure-database/ba-p/369142)

## **Recommended Steps**
* Ensure that there are no changes to the pricing tier of your service that might have triggered the increase.
* Adjust the pricing tier commensurate to the increase in the workload.
* Check if there are any schema changes, for example whether an index was dropped.
* Ensure that the table statistics are up to date. Run Analyze after a newly created index. 
* Determine when your tables were last vacuumed and tune threshold parameters (see **Recommended Documents** section)
* Check if there is a spike in short-lived connections, new connection requests or idle connections. 
* Enable Query Store to see any changes in the workload or query regression. Refer to [Performance Troubleshooting with Query Store](https://azure.microsoft.com/blog/performance-troubleshooting-using-new-azure-database-for-postgresql-features/)

## **Recommended Documents**

* [Performance Recommendations in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)
* [Optimize autovacuum on Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/howto-optimize-autovacuum)
* [Azure Database for PostgreSQL performance Quick Tips - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-postgresql-performance-quick-tips/ba-p/369125)
