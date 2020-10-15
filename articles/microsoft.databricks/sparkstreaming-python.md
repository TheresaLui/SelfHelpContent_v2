<properties
	pageTitle="Diagnose and resolve issues Python"
	description="Diagnose and resolve issues with Python"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32681391"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="88ad121d-7411-4048-99e5-183858990972"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Python

## **Recommended Steps**

* **Problem**

  Receiver is failing for a case of data being expired getting error similar to:
  
  ```
  request seqNo xxxxx is less than the received seqNo
  requestSeqNo does not match the received seqNo
  ```
  
  **Solution**
  
  Please make sure to use the [latest connector version](https://mvnrepository.com/artifact/com.microsoft.azure/azure-eventhubs-spark) available.
  
* **Problem**

  Getting exception ```java.lang.IllegalArgumentException: Input byte array has wrong 4-byte ending unit.``` which is thrown because starting from version 2.3.15, pyspark requires the connection string be encrypted when it's passed to the configuration dictionary. 
  
  **Solution**
  
  Encrypt the connection string by using the following method:
  
  ```
  ehConf['eventhubs.connectionString'] = sc._jvm.org.apache.spark.eventhubs.EventHubsUtils.encrypt(connectionString)
  ```

## **Recommended Documents**

* [Structured Streaming Demo in Python](https://docs.databricks.com/spark/latest/structured-streaming/demo-notebooks.html#structured-streaming-python)

