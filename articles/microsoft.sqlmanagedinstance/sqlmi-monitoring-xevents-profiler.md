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

**Extended Events**
The [Extended Events](https://docs.microsoft.com/sql/relational-databases/extended-events/extended-events?view=sql-server-ver15) architecture enables users to collect as much or as little data as is necessary to troubleshoot or identify a performance problem. Extended Events is configurable, and it scales very well.
Extended Events is a lightweight performance monitoring system that uses minimal performance resources. By using extended events, you can see details about the inner operations of the SQL system.
The bulk of our documentation about extended events applies to SQL Server, Azure SQL Database, and Azure SQL Managed Instance.

**SQL Profiler**
[SQL Server Profiler](https://docs.microsoft.com/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15) is an interface to create and manage traces and analyze and replay trace results.

### **Limitations\differences from SQL Server**
- **Extended Events**
  - Some Windows-specific targets for Extended Events (XEvents) aren't supported:
    - The etw_classic_sync target isn't supported. Store .xel files in Azure Blob storage. See [etw_classic_sync target](https://docs.microsoft.com/sql/relational-databases/extended-events/targets-for-extended-events-in-sql-server#etw_classic_sync_target-target).
    - The event_file target isn't supported. Store .xel files in Azure Blob storage. See [event_file target](https://docs.microsoft.com/sql/relational-databases/extended-events/targets-for-extended-events-in-sql-server#event_file-target).
  - Some Transact-SQL code examples written for SQL Server on-premises need small changes to run on Azure SQL Database service in the Cloud.
    - **server_**   -   prefix for on-premises (Ex.: server_event_session_actions)
    - **database_**   -   prefix for Azure SQL Database (Ex.: database_event_session_actions)
- **SQL Profiler**
  - SQL Trace and SQL Server Profiler are deprecated. **Use Extended Events instead**.
  - Azure SQL Database is not supported by SQL Server profiler, Managed Instance is supported.
  - SQL Profiler doesn’t capture all events and data Extended Events capture.

### **My session has stopped**
- To be sure that after SQL service restart your Extended Event also start create or change your session to use the following option "**WITH (STARTUP_STATE=ON)**"  
```CREATE EVENT SESSION [<xevent_name>] ON SERVER WITH (STARTUP_STATE=ON)```

### **Can’t save Extended Events session data capture into a file**
- Follow the steps from this article to save the captured data into a Azure Storage blob: [Extended Events capture step by step walkthrough](https://techcommunity.microsoft.com/t5/azure-database-support-blog/extended-events-capture-step-by-step-walkthrough/ba-p/369013)

### **Permissions to run SQL Profiler**
- User need to have ALTER TRACE permission  
```GRANT ALTER TRACE TO [username]```

### **Performance impact when using SQL Profiler**
- Try using Extended events it will cause less performance impact.
- Try [SQL Server Profiler extension](https://docs.microsoft.com/sql/azure-data-studio/extensions/sql-server-profiler-extension?view=sql-server-ver15) for Azure Data Studio, it uses Extended Events
- Confirm if [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15) have the required information 
- Avoid running from a local machine, try running from an Azure VM located on the same region as the Managed Instance.

### **Can’t capture data using Server Side Traces**
- Server side trace don’t support saving to a table and can’t save to a local file
- [Convert your SQL Trace script to an Extended Events Session](https://docs.microsoft.com/sql/relational-databases/extended-events/convert-an-existing-sql-trace-script-to-an-extended-events-session?view=sql-server-ver15)

### **Taking too long to do a trace without SQL Profiler**
- Try [SQL Server Profiler extension](https://docs.microsoft.com/sql/azure-data-studio/extensions/sql-server-profiler-extension?view=sql-server-ver15) for Azure Data Studio
- Create a Extended Events session to capture what is needed and when finish do not drop the session leave it there with the state 'STOP' to be reused when needed.  

```
ALTER EVENT SESSION [YourSession]
      ON SERVER
    --ON DATABASE
    STATE = START;   -- STOP;
```

## **Recommended documents**
- Azure SQL DB: [Extended events in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/xevent-db-diff-from-svr)
- [Quickstart: Extended events in SQL Server](https://docs.microsoft.com/sql/relational-databases/extended-events/quick-start-extended-events-in-sql-server?view=sql-server-ver15)
- [Create a Trace (SQL Server Trace)](https://docs.microsoft.com/sql/tools/sql-server-profiler/create-a-trace-sql-server-profiler?view=sql-server-ver15)
- [View the Extended Events Equivalents to SQL Trace Event Classes](https://docs.microsoft.com/sql/relational-databases/extended-events/view-the-extended-events-equivalents-to-sql-trace-event-classes?view=sql-server-ver15)
