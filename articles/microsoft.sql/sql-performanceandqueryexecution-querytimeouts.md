<properties
	pageTitle="Resolve poor query timeout performance issues in Azure SQL Database"
	description="Resolve poor query timeout performance issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
 	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749520"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-querytimeouts"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve poor query timeout performance issues in Azure SQL Database

### **Command Timeout**

In general command timeouts can be investigated using [query data store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15 ),where exec_type = 3 captures queries with a timeout.

That said, using wait stats for failed queries we can understand the bottlenecks; in many cases. Follow the document [Investigate Waitstats](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15#Waiting) to further analyze waits.

If the query bottleneck on IO: 
* Increase the query timeout
* Further optimize query if possible
* If query must perform lots of IOs and is latency sensitive than latencies per IO are better in BC offers

If the query bottleneck is on CPU:
* Check other CPU intensive activities
* Find of that is due to any other user load
* Optimize or [batch](https://docs.microsoft.com/azure/azure-sql/performance-improve-use-batching) the query or scale the database

### **Connection Timeout**

For DTU bases SLO's Azure SQL is using DTU as a measure of how many resources you use like CPU, IO and so on. So if you are using 100% of DTU your queries will be delayed and  you will get timeout exception. By default there is 30 seconds timeout in .net connection . Increasing will probably not help you since issue could be that you are running same query many times and it starts blocking each other.

Go to your database then Query Performance Insight, and see your top queries run time. And start optimisation from there.
Potential places could be EntityFramework (if you are using it), this could generate queries with huge amount of data to be returned which slows down query and uses lots of IO.

If you still want to increase timeout you can do that in [.config](https://docs.microsoft.com/dotnet/api/system.data.sqlclient.sqlconnection.connectiontimeout?redirectedfrom=MSDN&view=dotnet-plat-ext-3.1#System_Data_SqlClient_SqlConnection_ConnectionTimeout) file for your connection string by adding `;Connection Timeout=<value>`.

## **Recommended Documents**

* [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview?WT.mc_id=pid:13491:sid:32630450/).

