<properties
	pageTitle="Resolve other performance related errors and exceptions"
	description="Resolve other performance related errors and exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749519"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-othererrorsandexceptions"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve other performance related errors and exceptions

## **Recommended Documents**

Use [this reference](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues?WT.mc_id=pid:13491:sid:32630429/) to prevent, troubleshoot, diagnose, and mitigate connection errors and transient errors that your client application encounters when it interacts with Azure SQL Database. 

For further information about specific error codes, see [SQL error codes for SQL Database client applications](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages) and [database engine error messages](https://docs.microsoft.com/sql/relational-databases/errors-events/database-engine-events-and-errors?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630429/) 

Information about troubleshooting specific common errors is given in the following sections.  

### Error 701: There is insufficient system memory to run this query

SQL Server has failed to allocate sufficient memory to run the query. This can be caused by a variety of reasons including operating system settings, physical memory availability, or memory limits on the current workload. In most cases, the transaction that failed is not the cause of this error.See [this reference](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-701-database-engine-error?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630429/) for assistance in troubleshooting this error. 

### Error 10930: The service is currently too busy

Standardize a way to easily and consistently test network latency and bandwidth between two hosts, as well as look at the Azure network to help isolate problem points by using [this reference](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-network-performance?WT.mc_id=pid:13491:sid:32630429/). <br>

### Error 845: Time-out occurred while waiting for buffer latch type X for page Y database ID Z

A process was waiting to acquire a latch, but the process waited until the time limit expired and failed to acquire one. This can occur if an I/O operation takes too long to complete, usually as a result of other tasks blocking system processes. See [this reference](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-845-database-engine-error?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630429/) for assistance in troubleshooting this error. 

