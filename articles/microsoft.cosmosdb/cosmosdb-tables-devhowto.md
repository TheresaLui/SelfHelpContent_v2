<properties
	pageTitle="Azure Cosmos DB Tables" 
	description="Azure Cosmos DB Tables"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636750"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-tables-devhowto"
	displayOrder="300"
	category="Azure Table"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Tables 
Most users are able to resolve their Azure Cosmos DB Table issue using the steps below.  

## **Recommended Steps**  

### **Developing applications with Azure Cosmos DB Table API**

Applications written for Azure Table storage can migrate to Azure Cosmos DB by using the Table API.

To get started:

* Replace your connection string to connect to an Azure Cosmos DB account created with the Table API.
* Make sure to use the latest version of your Azure Table Storage driver or SDK; if your application is running on .NET, we recommend to use the [Azure Cosmos DB Table .NET Standard SDK](https://docs.microsoft.com/azure/cosmos-db/table-sdk-dotnet-standard).
* Get familiar with Azure Cosmos DB's provisioned throughput model and evaluate how many [Request Units](https://docs.microsoft.com/azure/cosmos-db/request-units) your application might need.

Then, learn about the premium capabilities you can leverage:

* Automatic secondary indexing: all columns get automatically indexed by default
* [Global distribution](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally): tables can be replicated to any Azure datacenter to ensure low latency and high availability

### **Changing throughput in Table API using .NET SDK**

If you are having troubles changing throughput using the .NET SDK, make sure to update it to the latest version [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet)  

Solution:
* Sample code to change the throughput in table api using .NET SDK [Easier APIs for scaling throughput](https://azure.microsoft.com/blog/new-for-developers-azure-cosmos-db-net-sdk-v3-now-available/).



### **Not able to create a Table via Portal**
If you are having troubles with Table API table creation via Portal.  
Solution:
* You can create table using SDK  *client.GetTableReference("OperationResults").CreateIfNotExists()*  


### **Exporting to a json file or Migrating data**
If you need to migrate data to Azure table or export to a json file.  

Solution:
* We recommend migrating data from Cosmos Table API using [Data Migration Tool](https://docs.microsoft.com/azure/cosmos-db/table-import#data-migration-tool)
* Sample below to migrate data from Cosmos Table API to a JSON file  

```
dt /s:AzureTable 
/s.ConnectionString:DefaultEndpointsProtocol=https;
AccountName=<Azure Table storage account name>;
AccountKey=<Account Key>;
TableEndpoint=https://<Azure Table storage account name>.documents.azure.com; 
/s.Table:<Table name>
/t:TableAPIBulk 
/t:JsonFile 
/t.File:C:<json file directory on local machine> 
/t.Overwrite
```



## **Recommended Documents**

[Introduction to Azure Cosmos DB: Table API](https://docs.microsoft.com/azure/cosmos-db/table-introduction)
<br>This article provides an introduction to the Table API for applications that are written for Azure Table storage.  

[Azure Storage Table Design Guide: Designing Scalable and Performant Tables](https://docs.microsoft.com/azure/cosmos-db/table-storage-design-guide)
<br>To design scalable and performant tables, you must consider a variety of factors, including cost. If you've previously designed schemas for relational databases, these considerations will be familiar to you. But while there are some similarities between Azure Table storage and relational models, there are also many important differences. These differences typically lead to different designs that might look counter-intuitive or wrong to someone familiar with relational databases, but that do make sense if you're designing for a NoSQL key/value store, such as Table storage.  

[Migrate your data to Azure Cosmos DB Table API account](https://docs.microsoft.com/azure/cosmos-db/table-import)
<br>This tutorial provides instructions on importing data for use with the Azure Cosmos DB Table API.