<properties
	  pageTitle="Check the Backend Total Duration"
	  description="Check the Backend Total Duration"
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
	  articleId="2e43a37c-7b37-4f51-acf3-543900b7edeb"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check the Backend Total Duration

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 
1. First you will need a narrow Time window in UTC to isolate the customer issue.

2. Check if the Backend is observing high latencies (comparable to what customer is complaining about). Use this query to see if there are latencies that are high in Backend. Replace the account name, TimeStamps in the query. If the latency is Known for a specific kind of request, additional where clause by OperationType , ResourceType 

- [Enum: Operation Type](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237523)
- [Enum: Resource Type](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237513)
<br>

```
BackendEndRequest5M
| where TIMESTAMP >  datetime(2019-04-01 20:00:00) and TIMESTAMP<  datetime(2019-04-01 22:00:00)
    and GlobalDatabaseAccountName == "<name>"
| summarize DurationMS=max(MaxTimeMilliseconds)/10000 by bin(TIMESTAMP, 5m), OperationType, ResourceType, Region
```

**Note**: Please ensure that customer is making the calls to the same region that they are claiming based upon the information provided. If they are making **cross region calls**, they will see higher latencies.

If the latency in the Backend is not high, continue with client side investigation. Otherwise create an IcM for High Backend Latency

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query.

<!--/issueDescription-->

