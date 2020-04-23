<properties
	pageTitle="Cosmos DB Spark Connector"
	description="Cosmos DB Spark Connector"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
   	ms.author="bharathb, arramac"
	selfHelpType="generic"
	supportTopicIds="32636828"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sparkconnector"
	displayOrder="126"
	category="Tools and Connectors"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Azure Cosmos DB Spark Connector
Most users are able to resolve their Spark Connector issue using the steps below. 

## **Recommended Steps**
Please ensure you are using Cosmos DB Spark connector 1.3.5+ from Maven and Spark 2.4.0 for common reliability fixes.

### **Timed out waiting for server response**
Error: java.io.IOException Failed to write statements.
Having a high configuration value for your *spark.cassandra.output.concurrent.writes* may cause you to exceed your provisioned RUs.  Consider lowering the value of *spark.cassandra.output.concurrent.writes*.  Depending on your provisioned RUs you may need to lower this value to less than 15 or 10.  

### **Request rate too large**
If you are Receiving a Request rate too large error, consider increasing the configs for *query_maxretryattemptsonthrottledrequests* or *query_maxretrywaittimeinseconds*.  

### **Spark unable to use full provisioned RUs**
If your Spark job is unable to use your full provisioned RUs, review your partition key for hot spots, and tune the number of cores/executors to match the provisioned throughput (executor per 5-10k RU as a thumb rule), and review the data sort order for ordering skews (you may need to shuffle).  


###**What is the safe way to kill CosmosDB ChangeFeed Spark Streaming**
If you manually kill or stop the process, it might result in the change feed process to crash in the middle and the checkpoint file would have the details of the last successful complete (previous successful process). When you run the next job, change feed might send part of the data again till the point where it crashed. So, it would be better to handle on the client side to reprocess the data (or clean the duplicate data) based on the information from the checkpoint file. The new job will pick up from the point of the last checkpoint file. It would be based on the file system and on the spark job if the file that it is writing to will be closed safely. There is no data loss with the manual kills and restarting. 

## **Recommended Documents**  

[Azure Cosmos DB Spark Connector documentation](https://docs.microsoft.com/azure/cosmos-db/spark-connector)
<br>Microsoft Doc examples of Spark jobs with data stored in Azure Cosmos DB using the Cosmos DB Spark connector. Cosmos can be used for batch and stream processing, and as a serving layer for low latency access.  

[Apache Spark Connector for Azure Cosmos DB 2.4 Examples](https://github.com/Azure/azure-cosmosdb-spark/tree/2.4/samples)
<br>Apache Spark Connector for Azure Cosmos DB.  

[Azure Cosmos DB Spark Connector configuration references](https://github.com/Azure/azure-cosmosdb-spark/wiki/Configuration-references)
<br>Description of the available configurations of the Cosmos DB Spark Connector.  


