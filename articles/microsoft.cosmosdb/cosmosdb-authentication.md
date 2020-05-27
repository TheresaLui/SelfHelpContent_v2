<properties
	pageTitle="Authentication"
	description="Troubleshoot Azure Cosmos DB Authentication related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="generic"
	supportTopicIds="32636770"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-authentication"
	displayOrder="60"
	category="Core (SQL)"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Authentication in Azure Cosmos DB
Most users are able to resolve their Authentication case using the steps below.

## **Recommended Steps**

Azure Cosmos DB uses Hash-based Message Authentication Code (HMAC) for authorization. You can use either a master key, or a resource token to allow fine-grained access to a resource such as a document. For authentication related concepts in Azure Cosmos DB, see the following documentation:

## **Recommended Documents**

* [Securing access to Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data)
* [Access Control on Azure Cosmos DB Resources](https://docs.microsoft.com/rest/api/cosmos-db/access-control-on-cosmosdb-resources)
* [Azure Cosmos DB database security](https://docs.microsoft.com/azure/cosmos-db/database-security)
