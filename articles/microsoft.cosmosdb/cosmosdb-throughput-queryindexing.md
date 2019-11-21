<properties
	pageTitle="Azure Cosmos DB Query and Indexing"
	description="Azure Cosmos DB Query and Indexing"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32684529"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-throughput-queryindexing"
	displayOrder="246"
	category="Throughput and Scaling"
/>

# Azure Cosmos DB Query and Indexing


## **Recommended Steps**   

**Not able to update the default indexing policy on a restored collection**
<br>There is a *_self* parameter which is not getting updated with the new collectionid. This can happen while the new collection is getting created.  Once the collection create has succeeded, the *_self* tag would be populated.


**Saving changes to my indexing policy in portal appear to do nothing**  
<br>The poperties *kind*, *dataType*, and *precision* are no longer necessary to explicitly set and you can omit them from your indexing policy. [Indexing policy examples](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy#indexing-policy-examples)  





## **Recommended Documents**

[Indexing in Azure Cosmos DB - Overview](https://docs.microsoft.com/azure/cosmos-db/index-overview)
<br>The goal of this article is to explain how Azure Cosmos DB indexes data and how it uses indexes to improve query performance. It is recommended to go through this section before exploring how to customize indexing policies.  

[Indexing policies in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/index-policy)
<br>In some situations, you may want to override this automatic behavior to better suit your requirements. You can customize a container's indexing policy by setting its indexing mode, and include or exclude property paths.  

[Manage indexing policies in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy)  
<br>In Azure Cosmos DB, data is indexed following indexing policies that are defined for each container. The default indexing policy for newly created containers enforces range indexes for any string or number. This policy can be overridden with your own custom indexing policy.
