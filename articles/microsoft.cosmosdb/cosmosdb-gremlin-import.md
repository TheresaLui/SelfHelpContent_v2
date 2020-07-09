<properties
	pageTitle="Gremlin data import"
	description="Tools and connectors to import data into Gremlin account"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32675631"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-gremlin-import"
	displayOrder="181"
	category="Gremlin (Graph)"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Gremlin - Import

Most users are able to resolve their Gremlin data import issue using the steps below. 

## **Recommended Steps**  

### **Not able to deploy Cosmos DB using ARM template**
Error: New-AzResourceGroupDeployment : 14:33:26 - The deployment 'functions-cosmos-deploy' failed with error(s). Showing 1 out of 1 error(s).  
Status Message: Provided list of regions contains duplicate regions.  

Solution: Please see [Gremlin API Templates samples](https://docs.microsoft.com/azure/cosmos-db/resource-manager-samples).  


### **Perform bulk data generate or import in Cosmos DB for Gremlin (Graph)**
Please see 
- [Graph Bulk Executor](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-graph-dotnet): Tutorial Using the graph bulk executor .NET library to perform bulk operations in Azure Cosmos DB Gremlin API. 
- [PRE-RELEASE Ver: Microsoft.Azure.CosmosDB.BulkExecutor](https://www.nuget.org/packages/Microsoft.Azure.CosmosDB.BulkExecutor/2.4.1-preview): This client library enables client applications to perform bulk operations in Azure Cosmos DB for SQL, Gremlin and MongoDB APIs. This is a prerelease version of Microsoft.Azure.CosmosDB.BulkExecutor.




## **Recommended Documents**

[Cosmos DB Data Migration Tool](https://docs.microsoft.com/azure/cosmos-db/import-data)
<br> Can be used to insert documents that will be recognized as vertices or edges by Gremlin engine.  

[GraphFrames](https://spark-packages.org/package/graphframes/graphframes)
<br>This is a prototype package for DataFrame-based graphs in Spark. Users can write highly expressive queries by leveraging the DataFrame API, combined with a new API for motif finding. The user also benefits from DataFrame performance optimizations within the Spark SQL engine.

