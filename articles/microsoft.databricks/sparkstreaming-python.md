<properties
	pageTitle="Diagnose and resolve issues Python"
	description="Diagnose and resolve issues with Python"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32784350"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="88ad121d-7411-4048-99e5-183858990972"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Python

## **Recommended Steps**

* **Eventhub receiver is failing for a case of data being expired after getting error**

 Eventhub receiver is failing for a case of data being expired after getting an error similar to the following:
  
  ```
  request seqNo xxxxx is less than the received seqNo
  requestSeqNo does not match the received seqNo
  ```

Ensure that you use the [latest Eventhub-Spark connector version](https://mvnrepository.com/artifact/com.microsoft.azure/azure-eventhubs-spark) available.
  
* **Eventhub-Spark connector exception**

Eventhub-Spark connector exception `java.lang.IllegalArgumentException: Input byte array has wrong 4-byte ending unit` is thrown because starting from connector version 2.3.15, pyspark requires the connection string to be encrypted when it's passed to the configuration dictionary. 
    
Encrypt the connection string by using the following method:
  
  ```
  ehConf['eventhubs.connectionString'] = sc._jvm.org.apache.spark.eventhubs.EventHubsUtils.encrypt(connectionString)
  ```

## **Recommended Documents**

* [Apache Spark DStream is not supported](https://docs.microsoft.com/azure/databricks/kb/streaming/dstream-not-supported)
* [Structured Streaming Demo in Python](https://docs.databricks.com/spark/latest/structured-streaming/demo-notebooks.html#structured-streaming-python)

