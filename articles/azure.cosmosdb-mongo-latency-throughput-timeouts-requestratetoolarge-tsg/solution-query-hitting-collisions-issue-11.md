<properties
	  pageTitle="Query hitting collisions issue"
	  description="Query hitting collisions issue"
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
	  articleId="e55068c1-49a0-4e9a-b77d-4e30ff794c06"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Query hitting collisions issue

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 
When a query hits collisions, the customer visible outcome can be one of the following
- Query fails with "Request Rate is Large error"
- Query takes very long time to execute and/or hits a timeout issue.

For RequestRateIsLarge/Timeout issue, the error message should include an activity id.  If you have the activity id, then skip the below steps


To investigate latency issues for such queries, 
1. Ask the customer to execute the query once and record the timestamp.
2. Wait for 30 minutes for the logs to get uploaded to Kusto
3. Execute the below query and replace the accountName/Timestamp.  It should return the rows with the activity id for the successful request
```
SqlQueryExecMetrics 
| where DatabaseAccount == "<account-name>" 
   and TIMESTAMP >= datetime(2018-09-05 12:36:31.3986521)+5m 
   and TIMESTAMP <= datetime(2018-09-05 12:36:31.3986521)
```

**Customer message:**
Based on the troubleshooting step above, please share the known issue or solution to customer and share any necessary link.

#### Resolution

Migrate the customer collection/account to use IndexV2 following the steps at
[Index V2](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237343)

<!--/issueDescription-->

