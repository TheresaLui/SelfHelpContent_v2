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

Resolve performance issues due to poor query timeouts in Azure SQL Database.

### **Command Timeout**

Most command timeouts can be investigated using [query data store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15 ), where `exec_type = 3` captures queries with a timeout.

By using wait stats for failed queries, we can understand where bottlenecks occur in many cases. Follow the document [Investigate Waitstats](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15#Waiting) to further analyze waits.

If the query bottleneck is on the IO: 
* Increase the query timeout
* Further optimize query if possible
* If query must perform lots of IOs and is latency sensitive, latencies per IO are better in BC offers

If the query bottleneck is on the CPU:
* Check other CPU intensive activities
* Determine if the bottleneck is due to any other user load
* Optimize or [batch](https://docs.microsoft.com/azure/azure-sql/performance-improve-use-batching) the query, or scale the database

### **Connection Timeout**

- Use the [Azure SQL Connectivity Checker](https://github.com/Azure/SQL-Connectivity-Checker) to help to narrow down the potential causes of connectivity failure. The PowerShell script in the link will run some connectivity checks from this machine to the server and database. 

- If the tool provides a recommended action, try to implement that action. If the issue persists, it most likely due to a connectivity issue rather than performance problem and we recommend filing a case under the support topic of connectivity to get appropriate assistance.

**If the tool did not provide a recommended action, review the following:**

For DTU bases, SLO's Azure SQL is using DTU as a measure of how many resources you use (such CPU, IO, and so on). If you're using 100% of DTU, your queries will be delayed and you'll get a timeout exception. By default there is 30 seconds timeout in `.net` connection . Increasing this will probably not help you, because the issue could be that you are running the same query repeatedly, and the queries are blocking each other.

- Go to your database adn select Query Performance Insight to see the runtime for your top queries. Start optimizations from there.
Potential areas to optimize are be **EntityFramework** if it's in use. This can generate queries with huge amount of data to be returned, which slows down query and uses lots of IO.

- If you still want to increase timeout, do that in the [.config](https://docs.microsoft.com/dotnet/api/system.data.sqlclient.sqlconnection.connectiontimeout?redirectedfrom=MSDN&view=dotnet-plat-ext-3.1#System_Data_SqlClient_SqlConnection_ConnectionTimeout) file for your connection string by adding `;Connection Timeout=<value>`.

## **Recommended Documents**

* [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview?WT.mc_id=pid:13491:sid:32630450/).

