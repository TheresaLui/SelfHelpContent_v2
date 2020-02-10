<properties
	pageTitle="Cosmos DB Spark Connector"
	description="Cosmos DB Spark Connector"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas, arramac"
   	ms.author="bharathb, arramac"
	selfHelpType="generic"
	supportTopicIds="32636828"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-sparkconnector"
	displayOrder="126"
	category="Tools and Connectors"
/>
# Azure Cosmos DB Spark Connector

## **Recommended Steps**

* Please upgrade to Cosmos DB Spark connector 1.3.5+ from Maven and Spark 2.4.0 for common reliability fixes.
* Import the uber jar from the Maven drop location above. There is a known issue with using Maven coordinates in Azure Databricks.
* If you run into "Request rate too large", you may have to increase the configs for `query_maxretryattemptsonthrottledrequests` or `query_maxretrywaittimeinseconds`
* If your Spark job is unable to use your full provisioned RUs, review your partition key for hot spots, and tune the number of cores/executors to match the provisioned throughput (executor per 5-10k RU as a thumb rule), and review the data sort order for ordering skews (you may need to shuffle)

## **Recommended Documents**

* [Azure Cosmos DB Spark Connector documentation](https://docs.microsoft.com/azure/cosmos-db/spark-connector)
* [Azure Cosmos DB Spark Connector Github project](https://github.com/Azure/azure-cosmosdb-spark/tree/master)
* [Azure Cosmos DB Spark Connector configuration references](https://github.com/Azure/azure-cosmosdb-spark/wiki/Configuration-references)
* [Creating Hive tables with Azure Cosmos DB as the data source](https://github.com/Azure/azure-cosmosdb-spark/wiki/Connecting-Cosmos-DB-with-PowerBI-using-spark-and-databricks-permium#creating-hive-spark-table-with-cosmos-db-data-source)
