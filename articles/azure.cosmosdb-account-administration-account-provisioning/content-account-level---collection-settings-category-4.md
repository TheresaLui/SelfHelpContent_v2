<properties
	  pageTitle="Account Level & Collection Settings Category"
	  description="Account Level & Collection Settings Category"
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
	  articleId="ff83c893-7f60-4a20-92cb-f6f9533a2c8d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Account Level & Collection Settings Category

This will help you to pull the information from the Azure Portal Telemetry. The Azure Portal Telemetry is logged when the user access the portal. So, the data would be available till the last time the portal was accessed.

You need access to the Azure Portal Telemetry:  
Please see: https://github.com/Azure/portaldocs/blob/d2d164db30647308788333635f59115116ec6fdc/portal-sdk/generated/top-telemetry.md

**Account Level Settings**
* Consistency Level  
* Is Multi Master Enabled
* Firewall Setting - This can be also found from the IP Firewall through MgmtGlobalDatabaseAccountTrace
* Failover Policy
 
**Collection Level Setting**
* Index Policy
* TTL Setting - Again this can be from the TTL Table from Kusto. Refer
* [TSG: Understanding TTL behavior and tracking](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237016)

**Partition Key**  
* Scale Throughput Change

##Firewall Rule Settings
Firewall Rule Setting can be found through the below query

```
MgmtGlobalDatabaseAccountTrace
| where GlobalDatabaseAccount =="testmigrationtool" and TIMESTAMP  > ago(1d)   
| project TIMESTAMP, Tenant, Level, EventId,Pid, Tid, ActivityId, GlobalDatabaseAccount, SubscriptionId
```

##Scale Throughput Change
The below query does return the Scale Throughput change along with the user who performed the scale throughput change.

**ATTENTION:** Please do not share the email address to customer.  You need to request customer the list of user who have access to the account from which you and point the user who performed the change.

```
let ago_time=time(3d);
let dbaccountname="cwp-device-api";
ExtTelemetry
| where extension == "Microsoft_Azure_DocumentDB"
| where action =="ScaleThroughput"
| where TIMESTAMP > ago(ago_time)
//| where TIMESTAMP >= todatetime("2019-03-16 15:10:00.0000000")
//| where TIMESTAMP <= todatetime("2019-03-16 15:20:00.0000000")
| where tostring(parse_json(['data'])) contains dbaccountname //and tostring(parse_json(['data'])) contains "Extension/Microsoft_Azure_DocumentDB/Blade/OverviewBlade"
| project TIMESTAMP, sessionId, ['data'], userId
| join  ( SvcSessions ) on sessionId  
| project TIMESTAMP, ['data'], email
```

**Note 1:**  The "ScaleThroughput" action is not logged on regular scale change in the portal. It would be logged when the portal recommends the user to scale up and they perform the action would log the telemetry. However, we have a request in place to log all the scale action from the portal which is would be available near future.  

 
**Note 2:** connect to endpoint azportalpartner.kusto.windows.net to access ExtTelemetry

##Collection Level Settings
Kusto cluster : Azportalpartner  
Database : AzurePortal

```

let ago_time=time(4d);
let dbaccountname="sql50gb";
ExtTelemetry
| where extension == "Microsoft_Azure_DocumentDB" and TIMESTAMP > ago(ago_time) and action =="LoadCollections"
| where tostring(parse_json(['data'])) contains dbaccountname and tostring(parse_json(['data'])) contains "Extension/Microsoft_Azure_DocumentDB/Blade/OverviewBlade"
| where tostring(parse_json(['data'])) contains "indexingPolicy"
//| project TIMESTAMP,CollectionProperties = tostring(parse_json(['data'])), action, context, objectId , extension, name, ProviderName, assetType, TaskName
| summarize max(TIMESTAMP) , min(TIMESTAMP) by tostring(parse_json(['data']))
```

