<properties
	  pageTitle="High SQL Query Latency issue"
	  description="High SQL Query Latency issue"
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
	  articleId="755bdf17-79ed-4d97-ab86-0603805fe71b"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# High SQL Query Latency issue

The below query would return any changes to the Index Version Schema and gives the time when the index version got changed.

Please provide the collection rid you are checking for.

```
ReportQuota5M
| where CollectionRid == "COLLECTIONRID"
| summarize min(TIMESTAMP), max(TIMESTAMP) by GlobalDatabaseAccountName, CollectionName, CollectionRid, IndexingSchemeVersion
```

