<properties
    pageTitle="Database X on server Y is not currently available"
    description="Database X on server Y is not currently available"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745430"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="E8D094DB-9BC4-40D3-8C7A-41CD46189C84"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Database X on server Y is not currently available

## **Recommended Steps**

### Error 40613: Database X on server Y is not currently available
* You will receive error 40613 when the connection to the SQL Database fails due to:

 - **Reconfiguration** - Reconfigurations can be caused by planned events (Ex. Software upgrades) or unplanned events (Ex. Process crash or load balancing). Most reconfiguration events are generally short lived, however these events can occasionally take longer to finish (Ex. Long-running transactions can cause long-running recovery).
 - **DAC Connections** - DAC (Dedicated Admin Connection) limits maximum number of admin connections to the database to only one. In this scenario, you will receive an error:
 
```
   "17810, Severity: 20, State: 2. \<Timeframe\> Could not connect because the maximum number of '%1' dedicated administrator connections already exists. Before a new connection can be made, the existing dedicated administrator connection must be dropped, either by logging off or ending the process.".
```
Dedicated Admin connection for administrators are solely for diagnosing under rare circumstances and with limitations. To guarantee that there are resources available for the connection, only one DAC is allowed at a time. If you experience the above error, please ensure to disconnect the existing DAC connection prior to attempting a new DAC connection. For more information, please visit [Diagnostic Connection for Database Administrators](https://docs.microsoft.com/sql/database-engine/configure-windows/diagnostic-connection-for-database-administrators?WT.mc_id=pid:13491:sid:32745425).
* For additional information, please refer to [Transient errors](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database?WT.mc_id=pid:13491:sid:32745425/#transient-fault-error-messages-40197-40613-and-others)

