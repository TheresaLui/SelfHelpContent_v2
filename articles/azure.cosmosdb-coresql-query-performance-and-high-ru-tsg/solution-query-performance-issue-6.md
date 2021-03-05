<properties
	  pageTitle="Query Performance issue"
	  description="Query Performance issue"
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
	  articleId="d0de08dd-0689-40ae-a7a5-7511b5f8667f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Query Performance issue

<!--issueDescription-->

Dear customer,

This Guide should provide you information how to assist a in case you are experiencing slow performance from SQL Query.

### Tuning Query Performance with Azure Cosmos DB
https://docs.microsoft.com/en-us/azure/cosmos-db/sql-api-query-metrics


## Slow performance receiving documents
**SQL API/.Net**
Identify what page size you are using and size of the documents.
 
In case your customer document size is on the larger size, 20+ kb, and your page size set to 100.   It is recommended for you to change the page size to (-1) rather than 100, as this causes added latency due to roundtrips to the server.  Additionally it id recommended  to project fewer items than the entire document, doing so would help return more documents per roundtrip since we can fit more documents into the response size limit.

Thank you.

<!--/issueDescription-->

