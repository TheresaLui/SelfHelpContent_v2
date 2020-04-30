<properties
	pageTitle="Azure Cosmos DB - Architecture and design"
	description="Troubleshoot Azure Cosmos DB - Architecture and design related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636768"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-architecture-design"
	displayOrder="41"
	category="General Advisory"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB - Architecture and design
Most users are able to resolve their Architecture and design issue using the steps below.

## **Recommended Steps**  

### **Sending data from CosmosDB to SQL Database or similar structured database**
If you have questions regarding how you can send data from CosmosDB to a SQL or similar structured database.
* **Cosmos DB SQL API:** [Copy and transform data in Azure Cosmos DB (SQL API) by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db) This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB (SQL API), and use Data Flow to transform data in Azure Cosmos DB (SQL API) 
* **MongoDB API:** [Copy data to or from Azure Cosmos DB's API for MongoDB by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)  

### **Managing your own backups**
We have some suggestions for how you can clone your Cosmos DB to another Resource Group or even to the same RG to manage your own backups:
* You can use the [Cosmos DB Data Migration tool](https://azure.microsoft.com/updates/documentdb-data-migration-tool/). With the Azure Cosmos DB Data Migration tool you can easily migrate data to Azure Cosmos DB. The Azure Cosmos DB Data Migration tool is an open source solution.
* You can use Azure Data Factory (ADF), using ADF you can copy data from Azure Cosmos DB (SQL API) to another Azure Cosmos DB (SQL API)  

### **Reducing need for backups**
Your Cosmos DB account may not require backup/restore for disaster recovery. Azure Cosmos DB provides [High availability with Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/high-availability) to transparently replicate your data across all the Azure regions associated with your Cosmos account.  


## **Recommended Documents**  
[How to model and partition data on Azure Cosmos DB using a real-world example](https://docs.microsoft.com/azure/cosmos-db/how-to-model-partition-example)
<br>This article builds on several Azure Cosmos DB concepts like data modeling, partitioning, and provisioned throughput to demonstrate how to tackle a real-world data design exercise.  

[Use custom activities in an Azure Data Factory pipeline](https://docs.microsoft.com/azure/data-factory/transform-data-using-dotnet-custom-activity)
<br>This article covers two types of activities that you can use in an Azure Data Factory pipeline:
* Data movement activities to move data between supported source and sink data stores
* Data transformation activities to transform data using compute services such as Azure HDInsight, Azure Batch, and Azure Machine Learning