<properties
	  pageTitle="Connectiviy Issues troubleshooting"
	  description="Connectiviy Issues troubleshooting"
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
	  articleId="ab91591e-904e-4c07-a477-e5f2d90bf977"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Connectiviy Issues troubleshooting

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Troubleshooting:**

#### Get the CosmosDB connection GUID from the client connectionId
CosmosDB Mongo api assigns a unique GUID to each connection. Use the below kusto query to get the ConnectionGuid from the client-side connectionId

```
let startTime=<>;
let endTime=<>;
let connectionId="";
ComputeDebug
| where TIMESTAMP >= startTime and TIMESTAMP <= endTime
| where Message contains "[MongoApi]" and Message contains connectionId
| extend ConnectionId=extract("\\[MongoApi\\] \\[([a-zA-Z0-9-]*)\\] \\[", 1, Message, typeof(string))
| distinct ConnectionId
```
Example:
https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/ERo1CHYFVHREj43gccAt0LYByiu5K_WdDVYsXO9LkgtTAw?e=3YepRr

<br>
<br>

#### Find the connection closure reason from the CosmosDB connection GUID

Use the below kusto query to get all the logs for the given connection, including the closure reason

```
let startTime=<>;
let endTime=<>;
let connectionGuid="";

ComputeDebug
| where TIMESTAMP >= startTime and TIMESTAMP <= endTime
| where Message contains connectionGuid
| project TIMESTAMP, ActivityId, Message
```
Example:
https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EQNyyIvPi_5DnywcfXd7-TYBIkGzmOsnh_mZnYFKGCKHLQ?e=WJp9VS


## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query.

<!--/issueDescription-->

