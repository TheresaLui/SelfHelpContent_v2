<properties
	  pageTitle="Query hitting retries on the server side issue"
	  description="Query hitting retries on the server side issue"
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
	  articleId="88c3a8e4-2280-418e-bd39-e8d9080efaa1"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Query hitting retries on the server side issue

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**CSS Investigation:**
Run the below query only for the time-period when the customer ran the repro

```
MongoProxyRequest5M
| where DatabaseAccountName == "<account-name>" 
   and CollectionName == "<collection-name>"
   and TIMESTAMP >= datetime(<start-repro-time>) 
   and TIMESTAMP <= datetime(<end-repro-time>)
| project TIMESTAMP, DatabaseName, CollectionName, CommandName, ErrorCode, SampleCount, MaxItemsImpacted, TotalItemsImpacted, MaxRequestCharge, TotalRequestCharge, Percentile99, MaxTimeInMilliseconds, MaxRetryCount, TotalRetryCount 
```

Look for rows with the below CommandNames, which is different for different types of request


| Query | OP_QUERY, OP_GETMORE, find, getMore |
|--|--|
| Aggregation | Aggregate |
| Count | Count |
| Update | Update, findAndModify |

For these entries, check if the MaxRetryCount/TotalRetryCount is value is greater than 0.  If yes, then the customers request are hitting rate-limiting (throttling).  The default Mongo api behavior is to retry for throttled request for up to 10 times and/or 15 seconds of execution, whichever is earlier.  Each time the request is retired, it adds an extra processing time + delay and hence the customer sees higher latency.

Thank you.

## Customer message:
Based on the troubleshooting step above, please share the known issue or solution to customer and share any necessary link.

<!--/issueDescription-->

