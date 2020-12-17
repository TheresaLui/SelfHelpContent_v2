<properties
	  pageTitle="Check if customer is using Composite Indexes"
	  description="Check if customer is using Composite Indexes"
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
	  articleId="0cafe6d9-fb3c-4a92-8453-8c55e36f93dd"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check if customer is using Composite Indexes

In case you want to know if customer is using Composite Indexes you can query MetricsIndexingPolicy5M table (per region) and check if the field MaxCompositePaths is greater than 0 (MaxCompositePaths > 0).

Please refer [How to determine Composite Index can help reduce RU Cost](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/343689/TSG-How-to-determine-Composite-Index-would-reduce-the-High-RU-cost)


Please find an example of a sample query below.

**Kusto query to confirm Composite Index usage:**
```
// Kusto Query to help understand if customer is using Composite Index.
// You must query MetricsIndexingPolicy5M table (per region)
MetricsIndexingPolicy5M
| where DatabaseAccount contains "ACCOUNTNAME"
| where CollectionId == "COLLECTIONID" 
| where MaxCompositePaths > 0 
| summarize by DatabaseAccount, CollectionId, MaxCompositePaths
```

<br>

**Important Notes:**

* Please don't forget you should use the query MetricsIndexingPolicy5M table per region.
* For more details about Composite Index please:
* * Check this link: https://docs.microsoft.com/en-us/azure/cosmos-db/index-policy#composite-indexes 
* * Watch this video: https://msit.microsoftstream.com/video/87de30ab-8b92-46f5-a93a-a132cb283942?st=787 

