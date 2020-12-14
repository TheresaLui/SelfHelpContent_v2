<properties
	  pageTitle="Know why the split occurred"
	  description="Know why the split occurred"
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
	  articleId="9d4bd5f6-f3e1-4987-96aa-551d491a24f0"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Know why the split occurred

<!--issueDescription-->

**Investigation (not customer message):**
Use the OperationQOSEvent table and look at the operationName property. 
- **ThroughputSplit**: User initiated the RU/s scale-up
- **SplitRange**: System initiated split due to storage increase

```
// The split was initiated due to user changing the RU/s - scaling up
OperationQOSEvent 
| where TIMESTAMP >= ago(6hr)
| where databaseAccount == "xxxxxx"
| where operationName == "ThroughputSplit"

// The split was initiated due to storage increase
OperationQOSEvent 
| where TIMESTAMP >= ago(6hr)
| where databaseAccount == "xxxxxx"
| where operationName == "SplitRange"
```

**Customer message:**
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->
