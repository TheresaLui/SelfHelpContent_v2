<properties
	  pageTitle="Check Index V2 with Full Fidelity"
	  description="Check Index V2 with Full Fidelity"
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
	  articleId="ca315c88-dcc9-4f7a-bddf-371e78d63c64"
	  ownershipId="AzureData_AzureCosmosDB"
/>

### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** Investigate based on the steps below.

#### Check Index V2 with Full Fidelity

<!--issueDescription-->

Index V2 with Full fidelity is the latest layout of Index V2. To check whether a container is full fidelity, you can use ReportQuota5M table (global table). A container can have Index V2, but may not be Full Fidelity. To be as much optimized as possible a container need to be Index V2 with Full Fidelity.

The product group (Query team) can help to move the Index V2 to Index V2 with Full Fidelity.


**Kusto query to check if customer containers are set as full fidelity:**
```
// Kusto Query which helps to check if the container is full fidelity. 
// Use Global table
// Note: that you'd need all 3 conditions to determine whether or not the query would consider a containerfull-fidelity 
let subscriptionId = "SUBSCRIPTIONID";
ReportQuota5M
| where SubscriptionId == subscriptionId
| where TIMESTAMP > now(-1h) and IndexingSchemeVersion == 2 and IndexEncodingOptions == 65551 and IndexingFullFidelityEnabled == 1
| distinct GlobalDatabaseAccountName, DatabaseName, CollectionName 
```

**Important Notes:**
* Note that you'd need all 3 conditions to determine whether or not the query would consider a collection full-fidelity
* You should use Global table in Kusto to execute this query.
* Every container which gets created now will have Index V2 full fidelity
* For more details about Full fidelity please watch the following video: https://msit.microsoftstream.com/video/87de30ab-8b92-46f5-a93a-a132cb283942?st=2219 


#### Other Notes:
In case you want to find the Index Version on a given collection, use the below Kusto query:
```
ReportQuota5M
| where GlobalDatabaseAccountName =="ACCOUNTNAME"
| summarize by CollectionName , CollectionRid , IndexingSchemeVersion
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query.

<!--/issueDescription-->

