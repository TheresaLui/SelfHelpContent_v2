<properties
	  pageTitle="Check for known issues and solutions"
	  description="Check for known issues and solutions"
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
	  articleId="97926623-c6ad-4a10-a040-799e61f95608"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check for known issues and solutions

**Inform customer about the Recommended steps:**

In order to achieve the best performance for Azure Cosmos DB MongoDB API, there are a few aspects you can configure:
* Collocate clients in same Azure region for performance
* Increase parallelism on the client whenever possible
* Use singleton Azure Cosmos DB client for the lifetime of your application
* Exclude unused paths from indexing for faster writes
* Design for smaller documents for higher throughput

## **Check Recommended Documents**
[Azure Cosmos DB's API for MongoDB (3.6 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>The Azure Cosmos DB's API for MongoDB is compatible with MongoDB server version 3.6 by default for new accounts. The supported operators and any limitations or exceptions are listed in this article. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.2 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support)
<br>This article covers MongoDB version 3.2. The supported operators and any limitations or exceptions are listed in this article.  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.

