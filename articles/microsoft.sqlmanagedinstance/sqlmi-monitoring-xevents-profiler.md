<properties
	pageTitle="Extended events and SQL Profiler issues with Managed Instance"
	description="Extended events and SQL Profiler issues with Managed Instance"
	infoBubbleText="Extended events and SQL Profiler issues with Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748862"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-monitoring-xevents-profiler.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Extended events and SQL Profiler issues with Managed Instance

Most users can resolve issues with Extended Events and SQL Profiler with Managed Instance, by following the information below.

**Extended Events**

The [Extended Events](https://docs.microsoft.com/sql/relational-databases/extended-events/extended-events?view=sql-server-ver15) architecture enables users to collect as much or as little data as is necessary to troubleshoot or identify a performance problem. Extended Events is configurable, and it scales very well.

Extended Events is a lightweight performance monitoring system that uses minimal performance resources. By using Extended Events, you can see details about the inner operations of the SQL system.

Most of our documentation about Extended Events applies to SQL Server, Azure SQL Database, and Azure SQL Managed Instance.

**SQL Profiler**

[SQL Server Profiler](https://docs.microsoft.com/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15) is an interface to create and manage traces and analyze and replay trace results.

### **Limitations and differences from SQL Server**

- **Extended Events**
  - Some Windows-specific targets for Extended Events (XEvents) aren't supported:
    - The etw_classic_sync target isn't supported. Store .xel files in Azure Blob storage. See [etw_classic_sync target](https://docs.microsoft.com/sql/relational-databases/extended-events/targets-for-extended-events-in-sql-server#etw_classic_sync_target-target).
    - The event_file target isn't supported. Store .xel files in Azure Blob storage. See [event_file target](https://docs.microsoft.com/sql/relational-databases/extended-events/targets-for-extended-events-in-sql-server#event_file-target).
  - Some Transact-SQL code examples written for SQL Server on-premises need small changes to run on Azure SQL Database service in the cloud:
    - **server_**   -   prefix for on-premises (Ex.: server_event_session_actions)
    - **database_**   -   prefix for Azure SQL Database (Ex.: database_event_session_actions)
- **SQL Profiler**
  - SQL Trace and SQL Server Profiler are deprecated. **Use Extended Events instead**.
  - Azure SQL Database is not supported by SQL Server profiler. Managed Instance is supported.
  - SQL Profiler doesn’t capture all events and data that Extended Events captures.

## **Recommended Steps**

### **My session has stopped**
- To ensure that after SQL service restarts, your Extended Event also starts, create or change your session: 
`CREATE EVENT SESSION [<xevent_name>] ON SERVER WITH (STARTUP_STATE=ON)`

### **Can’t save Extended Events session data capture into a file**
- To save the captured data into a Azure Storage blob, follow [these steps](https://techcommunity.microsoft.com/t5/azure-database-support-blog/extended-events-capture-step-by-step-walkthrough/ba-p/369013)

### **Permissions to run SQL Profiler**
- The user must have ALTER TRACE permissions: 
`GRANT ALTER TRACE TO [username]`

### **Performance impact when using SQL Profiler**
- Try using Extended Events. This will help to decrease incidents of performance impact.
- Try [SQL Server Profiler extension](https://docs.microsoft.com/sql/azure-data-studio/extensions/sql-server-profiler-extension?view=sql-server-ver15) for Azure Data Studio, which uses Extended Events
- Verify that [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15) has the required information 
- Avoid running from a local machine. Try running from an Azure VM located on the same region as the Managed Instance.

### **Can’t capture data using server-side tracing**
- If the server side trace doesn’t support saving to a table and you can’t save to a local file, follow the instructions at [convert your SQL Trace script to an Extended Events Session](https://docs.microsoft.com/sql/relational-databases/extended-events/convert-an-existing-sql-trace-script-to-an-extended-events-session?view=sql-server-ver15)

### **Takes too long to do a trace without SQL Profiler**
- Try [SQL Server Profiler extension](https://docs.microsoft.com/sql/azure-data-studio/extensions/sql-server-profiler-extension?view=sql-server-ver15) for Azure Data Studio
- Create an Extended Events session to capture what is needed. When finished, do not drop the session. Leave it as is, with the state `STOP`, to be reused when needed.  

```
ALTER EVENT SESSION [YourSession]
      ON SERVER
    --ON DATABASE
    STATE = START;   -- STOP;
```

## **Recommended Documents**

- [Extended Events in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/xevent-db-diff-from-svr)
- [Quickstart: Extended Events in SQL Server](https://docs.microsoft.com/sql/relational-databases/extended-events/quick-start-extended-events-in-sql-server?view=sql-server-ver15)
- [Create a trace (SQL Server trace)](https://docs.microsoft.com/sql/tools/sql-server-profiler/create-a-trace-sql-server-profiler?view=sql-server-ver15)
- [View the Extended Events equivalents to SQL trace event classes](https://docs.microsoft.com/sql/relational-databases/extended-events/view-the-extended-events-equivalents-to-sql-trace-event-classes?view=sql-server-ver15)
