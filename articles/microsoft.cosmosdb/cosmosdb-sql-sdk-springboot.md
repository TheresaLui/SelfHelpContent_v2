<properties 
	pageTitle="SDK springboot" 
	description="SDK springboot" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32783727"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-springboot"
	displayOrder="441"
	category="SDK Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

#  Azure Cosmos DB SDK Springboot 
Most users are able to resolve their SDK Springboot issue with the following steps.

## **Recommended Steps**  

### **Release and Version info**
- [Spring Data for Azure Cosmos DB](https://github.com/microsoft/spring-data-cosmosdb/releases)

###**Connection issues**
If you experience connection issues, be sure all the required annotations in the configuration class are present and correct, as described in the [Getting the correct Cosmos DB configuration](https://docs.microsoft.com/azure/developer/java/spring-framework/how-to-guides-spring-data-cosmosdb#getting-the-correct-cosmos-db-configuration) section.

###**API or query slowness**
If you experience high latencies on APIs or query executions, try logging diagnostics strings and query metrics as described in the Enable Diagnostics and Query Metrics](https://docs.microsoft.com/azure/developer/java/spring-framework/how-to-guides-spring-data-cosmosdb#enable-diagnostics-and-query-metrics) section. Check for CPU usage, network bandwidth, and I/O disk space, which can be the root causes of client-side slowness.


###**Unsupported feature on spring Data for Azure Cosmos DB**
- TTL
- Option for providing Multiple database account names
- Cosmos DB Change feed Library
- No Auto generation of ID value.  Natively spring boot users are used to the behaviour of ID auto generation.   But the spring data for Azure Cosmos DB does require to ID value to be provided.


## **Recommended Documents**  

[How to use the Spring Boot Starter with the Azure Cosmos DB SQL API](https://docs.microsoft.com/azure/developer/java/spring-framework/configure-spring-boot-starter-java-app-with-cosmos-db)
<br>This article demonstrates creating an Azure Cosmos DB using the Azure portal, then using the Spring Initializr to create a custom Spring Boot application, and then add the Spring Boot Cosmos DB Starter for Azure to your custom application to store data in and retrieve data from your Azure Cosmos DB by using Spring Data and the Cosmos DB SQL API.  

[Spring Data Azure Cosmos DB developer guide](https://docs.microsoft.com/azure/developer/java/spring-framework/how-to-guides-spring-data-cosmosdb)
<br>This topic describes the features of Spring Data Cosmos DB using the SQL API. This topic also includes guidance on common issues, workarounds, and diagnostic steps.
