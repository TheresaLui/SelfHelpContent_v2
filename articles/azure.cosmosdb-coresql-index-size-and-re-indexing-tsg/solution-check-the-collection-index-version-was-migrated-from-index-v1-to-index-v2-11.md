<properties
	  pageTitle="Check the Collection index version was migrated from Index V1 to Index V2"
	  description="Check the Collection index version was migrated from Index V1 to Index V2"
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
	  articleId="5d4b2e85-14c2-4131-a363-423f5cc33454"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check the Collection index version was migrated from Index V1 to Index V2

<!--issueDescription-->

The below query would return any changes to the Index Version Schema and gives the time when the index version got changed.

Please provide the collection rid you are checking for.

```
ReportQuota5M
| where CollectionRid == "D3wQALXlSQA="
| summarize min(TIMESTAMP), max(TIMESTAMP) by GlobalDatabaseAccountName, CollectionName, CollectionRid, IndexingSchemeVersion
```

|      |                           |                |               |                       |                             |                             |
| ---- | ------------------------- | -------------- | ------------- | --------------------- | --------------------------- | --------------------------- |
|      | GlobalDatabaseAccountName | CollectionName | CollectionRid | IndexingSchemeVersion | min_TIMESTAMP               | max_TIMESTAMP               |
|      | vl-db                     | c              | D3wQALXlSQA=  | 1                     | 2020-02-12 22:50:00.0000000 | 2020-02-26 13:55:00.0000000 |
|      | vl-db                     | c              | D3wQALXlSQA=  | 2                     | 2020-02-26 03:10:00.0000000 | 2020-02-27 01:55:00.0000000 |

**Customer message:**
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query.

<!--/issueDescription-->

