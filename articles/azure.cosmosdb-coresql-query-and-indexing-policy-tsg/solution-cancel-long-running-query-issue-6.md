<properties
	  pageTitle="Cancel long running query issue"
	  description="Cancel long running query issue"
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
	  articleId="91a63f3c-dd50-41ed-b4a7-4b966a9edf04"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Cancel long running query issue

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:**
Make sure to confirm customer executed an Expensive Query and wanted to cancel the Execution with no luck. If customer claims that the query has been running for a long time on the server based on their RUs observations, customer also noticed a spike in RU consumption and it matches the query execution time.

**Resolution:**
* The spikes in their request count may come from the SDK (for example the .NET SDK). Closing portal window, will stop the request. Please find more information in the comment below.
* From query engine perspective, each backend request is preempted after 4.5 seconds. A query can have multiple backend requests.
If the query was long running, there must have been many throttled requests. Please execute the below Kusto query:
```
BackendEndRequest5M
| where TIMESTAMP >= datetime(2020-01-02 13:15:00) - 4h and TIMESTAMP <= datetime(2020-01-02 13:15:00) + 4h
| where GlobalDatabaseAccountName contains "ACCOUNTNAME" and OperationType == 15
| summarize sum(SampleCount) by StatusCode
| sort by StatusCode asc
```
* When portal window is closed, there is nothing stateful about the query, it will totally stop. There is no other way, currently, to stop.

* Also, the spikes in customer requests may come from .net SDK, and not from portal. 
```
Request5M
| where globalDatabaseAccountName == "ACCOUNTNAME"
| where TIMESTAMP > ago(3d)
| summarize sum(SampleCount) by userAgent, bin(TIMESTAMP, 1h)
| order by userAgent asc
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query.

<!--/issueDescription-->

