<properties
	pageTitle="Extended events and SQL Profiler issues with Azure SQL Database"
	description="Extended events and SQL Profiler issues with Azure SQL Database"
	infoBubbleText="Extended events and SQL Profiler issues with Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32749525"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sql-monitoring-xevents-profiler.md"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve Extended events and SQL Profiler issues with Azure SQL Database

Most users can resolve issues regarding Extended Events and SQL Profiler issues with Azure SQL Database by following the information below.

**Extended Events**

The [Extended Events](https://docs.microsoft.com/sql/relational-databases/extended-events/extended-events?view=sql-server-ver15) architecture enables users to collect as much or as little data as is necessary to troubleshoot or identify a performance problem. Extended Events is configurable, and it scales very well.

Extended Events is a lightweight performance monitoring system that uses minimal performance resources. By using Extended Events, you can see details about the inner operations of the SQL system.

Most of our documentation about Extended Events applies to SQL Server, Azure SQL Database, and Azure SQL Managed Instance.

**SQL Profiler**

[SQL Server Profiler](https://docs.microsoft.com/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15) is an interface to create and manage traces and analyze and replay trace results.

### **Limitations\differences from SQL Server**
- **Extended Events**
  - Some Windows-specific targets for Extended Events (XEvents) aren't supported:
    - The etw_classic_sync target isn't supported. Store .xel files in Azure Blob storage. See [etw_classic_sync target](https://docs.microsoft.com/sql/relational-databases/extended-events/targets-for-extended-events-in-sql-server#etw_classic_sync_target-target).
    - The event_file target isn't supported. Store .xel files in Azure Blob storage. See [event_file target](https://docs.microsoft.com/sql/relational-databases/extended-events/targets-for-extended-events-in-sql-server#event_file-target).
  - Some Transact-SQL code examples written for SQL Server on-premises need small changes to run on Azure SQL Database service in the cloud:
    - **server_**   -   prefix for on-premises (Ex.: server_event_session_actions)
    - **database_**   -   prefix for Azure SQL Database (Ex.: database_event_session_actions)

- **SQL Profiler**
  - **Azure SQL Database is not supported by SQL Server profiler**. Managed Instance is supported.
  - SQL Trace and SQL Server Profiler are deprecated. **Use Extended Events instead**.
  - SQL Profiler doesn’t capture all the events and data that Extended Events captures
  
## **Recommended Steps**

### **My session has stopped**
- To ensure that after SQL service restarts, your Extended Event also starts, create or change your session: 

```
CREATE EVENT SESSION [<xevent_name>] ON SERVER WITH (STARTUP_STATE=ON)
```

### **Can’t save the Extended Events session data capture into a file**
- Follow [these steps](https://techcommunity.microsoft.com/t5/azure-database-support-blog/extended-events-capture-step-by-step-walkthrough/ba-p/369013) to save the captured data to a Azure Storage blob

### **Can’t run SQL Profiler on Azure SQL Database**
- Use Extended Events to [convert your SQL trace script to an Extended Events session](https://docs.microsoft.com/sql/relational-databases/extended-events/convert-an-existing-sql-trace-script-to-an-extended-events-session?view=sql-server-ver15)
- Try [SQL Server Profiler extension](https://docs.microsoft.com/sql/azure-data-studio/extensions/sql-server-profiler-extension?view=sql-server-ver15) for Azure Data Studio, which uses Extended Events

### **Taking too long to do a trace without SQL Profiler in Azure SQL Database**
- Try [SQL Server Profiler extension](https://docs.microsoft.com/sql/azure-data-studio/extensions/sql-server-profiler-extension?view=sql-server-ver15) for Azure Data Studio
- Create an Extended Events session to capture what is needed. When finished, don’t drop the session. Leave it as is, with the state `STOP`, to be reused when needed.  

```
ALTER EVENT SESSION [YourSession]
      ON SERVER
    --ON DATABASE
    STATE = START;   -- STOP;
```

## **Recommended Documents**

- [Extended events in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/xevent-db-diff-from-svr)
- [Quickstart: Extended events in SQL Server](https://docs.microsoft.com/sql/relational-databases/extended-events/quick-start-extended-events-in-sql-server?view=sql-server-ver15)
- [Create a Trace (SQL Server Trace)](https://docs.microsoft.com/sql/tools/sql-server-profiler/create-a-trace-sql-server-profiler?view=sql-server-ver15)
- [View the Extended Events equivalents to SQL trace event classes](https://docs.microsoft.com/sql/relational-databases/extended-events/view-the-extended-events-equivalents-to-sql-trace-event-classes?view=sql-server-ver15)
