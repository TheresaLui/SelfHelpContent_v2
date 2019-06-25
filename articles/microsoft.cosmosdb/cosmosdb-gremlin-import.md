<properties
	pageTitle="Gremlin data import"
	description="Tools and connectors to import data into Gremlin account"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32675631"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-import"
/>
# Gremlin - Data Import

Here are some of the ways data can be imported into Gremlin account: 

* [Graph Bulk Executor](https://docs.microsoft.com/en-us/dotnet/api/microsoft.azure.cosmosdb.bulkexecutor.graph?view=azure-dotnet)
* [Gremlin Kafka Connector](https://github.com/Azure/kafka-connect-cosmosdb-graph)
* [Cosmos DB Data Migration Tool](https://docs.microsoft.com/en-us/azure/cosmos-db/import-data) can be used to insert documents that will be recognized as vertices or edges by Gremlin engine.
* [Cosmos DB Spark Connector](https://github.com/Azure/azure-cosmosdb-spark#using-databricks-notebooks) with [GraphFrames](https://spark-packages.org/package/graphframes/graphframes)