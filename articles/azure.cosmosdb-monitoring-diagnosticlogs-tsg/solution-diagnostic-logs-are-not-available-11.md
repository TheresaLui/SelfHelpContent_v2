<properties
	  pageTitle="Diagnostic Logs are not available"
	  description="Diagnostic Logs are not available"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="cd6c0051-723d-49dd-a008-b774d2d83e4e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Diagnostic Logs are not available

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Investigation (not customer message):**
This TSG is to provide investigation steps that CSS engineers can follow against the issue with unavailable diagnostic logs.


### Azure CosmosDB Diagnostic Log overview
The logs are categorized into seven categories such as:  

- DataPlaneRequest
- QueryRuntimeStatistics
- PartitionKeyStatistics
- PartitionKeyRUConsumption
- MongoRequests
- CassandraRequests
- ControlPlaneRequest

This TSG is applied to all the categories.
 
### Diagnostic Log Owners
The following table shows the teams that are responsible to the categories in the diagnostic log.  Please consult with the corresponding teams for proper support.
|Category  | Owning Team  |
|--|--|
| DataPlaneRequest, QueryRuntimeStatistics, PartitionKeyStatistics, PartitionKeyRUConsumption | Monitoring Team   |
| MongoRequest | MongoDB API Team |
| CassandraRequest | Cassandra API Team  |
| ControlPlaneRequest | Management Service Team |

### Trouble Shooting Workflow

1. Run the query to identify the Primary Region for the given Cosmos DB Account.  Replace <globaldatabaseaccount> with a target account name in the query.

   ```
   BillingOffers5M
   | where GlobalDatabaseAccountName == <globaldatabaseaccount>
   | summarize by Region, AllowRead, AllowWrite
   ```

2. Check if the diagnostic settings have been enabled.  Replace <globaldatabaseaccount> with a target account name in the query.  If the value is false in the column that is corresponding to a diagnostic setting then it means the customer has not enabled the setting.  In this case, stop further investigation, and contact the customer asking for enabling the diagnostic setting.

   ```
   cluster('cdbsupport').database('Support').MgmtGlobalDatabaseAccountTrace
    | summarize maxTime = arg_max(PreciseTimeStamp, ConfigurationOverrides), minTime = arg_min(PreciseTimeStamp, ConfigurationOverrides) by SubscriptionId, GlobalDatabaseAccount, ResourceGroupName
    | extend enableDataPlaneRequestsTrace = extractjson("$.enableDataPlaneRequestsTrace", ConfigurationOverrides)
    | extend sqlQueryTextTraceType = extractjson("$.sqlQueryTextTraceType", ConfigurationOverrides)
    | extend enableMongoRequestsTrace = extractjson("$.enableMongoRequestsTrace", ConfigurationOverrides)
    | extend enableCassandraRequestsTrace = extractjson("$.enableCassandraRequestsTrace", ConfigurationOverrides)
    | extend enablePartitionKeyStatisticsTrace = extractjson("$.enablePartitionKeyStatisticsTrace", ConfigurationOverrides)
    | extend enablePartitionKeyMonitor = extractjson("$.enablePartitionKeyMonitor", ConfigurationOverrides)
    | extend enableControlPlaneRequestsTrace = extractjson("$.enableControlPlaneRequestsTrace", ConfigurationOverrides)
    | extend GlobalDatabaseAccountName = tolower(GlobalDatabaseAccount)
    | where GlobalDatabaseAccountName == tolower(<globaldatabaseaccount>)
    | project maxTime, minTime, SubscriptionId, GlobalDatabaseAccountName, enableDataPlaneRequestsTrace, sqlQueryTextTraceType, enableMongoRequestsTrace, enableCassandraRequestsTrace, enablePartitionKeyStatisticsTrace, enablePartitionKeyMonitor, enableControlPlaneRequestsTrace
   ```
1. Check if the customer has issued the requests that are eligible to diagnostic logs in an account during the given time window. In the case where the following queries do not emit any entry then pelease stop further investigation.  It means that the customer has not issued any requests that are eligible to diagnostic logs.  It is expected that the logs are not generated.

- For DataPlaneRequest,
  - Check the BackendEndRequest5M for Direct Connection Mode.  Please note the filtering conditions in the query.  We emit diagnostic logs only for particular operation and resource types.
   ```
   BackendEndRequest5M
   | where TIMESTAMP >= datetime(2020-03-30T15:27:41.518Z) - 30m and TIMESTAMP <= datetime(2020-03-30T15:27:41.518Z) + 30m
   | where GlobalDatabaseAccountName == <globaldatabaseaccount>
   | where OperationType == 0 or OperationType == 1 or OperationType == 2 or OperationType == 3 or OperationType == 4 or OperationType == 5 or OperationType == 9 or OperationType == 14 or OperationType == 15 or OperationType == 17 or OperationType == 18 or OperationType == 19 or OperationType == 20
   | where ResourceType == 0 or ResourceType == 1 or ResourceType == 2 or ResourceType == 3 or ResourceType == 4 or ResourceType == 5 or ResourceType == 109 or ResourceType == 110 or ResourceType == 111 or ResourceType == 113
   | where CallerId != "Gateway"
   | summarize count() by ResourceType, OperationType
   | order by ResourceType, OperationType
   ```
  - Check the Request5M for Gateway Connection Mode.  Please note the filtering conditions in the query.  We emit diagnostis logs only for particular verbs and categories.
   ```
   Request5M
   | where TIMESTAMP >= datetime(2020-03-30T15:27:41.518Z) - 30m and TIMESTAMP <= datetime(2020-03-30T15:27:41.518Z) +30m
   | where verb == "PUT" or verb == "GET" or verb == "DELETE" or verb == "POST"
   | where category == "Collection" or category == "CollectionFeed" or category == "Document" or category == "DocumentFeed" or category == "Attachment" or category == "AttachmentFeed" or category == "Database" or category == "DatabaseFeed" or category == "Permission" or category == "PermissionFeed" or category == "Offer" or category == "OfferFeed" or category == "StoredProcedure" or category == "StoredProcedureFeed" or category == "Trigger" or category == "TriggerFeed" or category == "UserDefinedFunction" or category == "UserDefinedFunctionFeed" or category == "User"
   | where globalDatabaseAccountName == <globaldatabaseaccount>
   | summarize count() by category, verb
   | order by category, verb asc 
   ```
Please refer to the following list for supported operation and resource types:
  - Direct mode
    - Operation type: Create, Update, Read, ReadFeed, Delete, Replace, Execute, SqlQuery, Query, JSQuery, Head, HeadFeed, Upsert
    - Resource type: Database, Collection, Document, Attachment, User, Permission, StoredProcedure, Trigger, UserDefinedFunction, Offer
  - Gateway mode
    - Operation type: Query, Create (POST), Update (PUT), Read (GET), Delete (DELETE)
    - Resource type: Collection, CollectionFeed, Document, DocumentFeed, Attachment, AttachmentFeed, Database, DatabaseFeed, Permission, PermissionFeed, Offer, OfferFeed, StoredProcedure, StoredProcedureFeed, Trigger, TriggerFeed, UserDefinedFunction, UserDefinedFunctionFeed, User


4. If the requests that are eligible to diagnostic logs have been emitted then check the [Jarvis](https://jarvis-west.dc.ad.msft.net/84E8C978).  Please adjust the time range and the resourceId in the query.  As noticed from the Jarvis DGrep query, the namespace is AzCdbProdDiagLogs.  The following table shows the event tables that correspond to diagnostic settings.

|Event Name|Diagnostic Setting|
|--|--|
|DiagLogsBEDataPlaneRequests, DiagLogsGWDataPlaneRequests|DataPlaneRequest|
|DiagLogsQueryRequestsNew|QueryRuntimeStatistics|
|DiagLogsPartitionKeyStatistics|PartitionKeyStatistics|
|DiagLogsPartitionKeyRUConsumption|PartitionKeyRUConsumption|
|DiagLogsMongoRequests, DiagLogsMongoComputeRequests|MongoRequests|
|DiagLogsCassandraComputeRequests|CassandraRequests|

5. If the Jarvis query returns data then it means that CosmosDB pushes the telemetry data into the Azure Diagnostics without any issue. 
6. If the Jarvis query returns data but a customer cannot retrieve the data from her/his destination storage (e.g. Log Analytics workspace) then it is an issue in the telemetry pipeline with pulling the data from the storage (in Step 5) to the Azure Monitoring RP.  Please contact the Azure Monitoring team to investigate further.

<!--/issueDescription-->

