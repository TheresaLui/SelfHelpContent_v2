<properties
	pageTitle="Throughput Min and Max RU"
	description="Throughput Min and Max RU"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636800"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-throughput-minmax-ru"
	displayOrder="245"
	category="Throughput and Scaling"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Throughput Min and Max RU

## **Recommended Steps**
The cost of all database operations is normalized by Azure Cosmos DB and is expressed by Request Units (or RUs, for short). You can think of RUs per second as the currency for throughput. RUs per second is a rate-based currency. It abstracts the system resources such as CPU, IOPS, and memory that are required to perform the database operations supported by Azure Cosmos DB.
The cost to read a 1 KB item is 1 Request Unit (or 1 RU). All other database operations are similarly assigned a cost using RUs. No matter which API you use to interact with your Azure Cosmos container, costs are always measured by RUs. Whether the database operation is a write, read, or query, costs are always measured in RUs.


The following image shows the high-level idea of RUs:  
![throughput visual](https://docs.microsoft.com/azure/cosmos-db/media/request-units/request-units.png)  


To manage and plan capacity, Azure Cosmos DB ensures that the number of RUs for a given database operation over a given dataset is deterministic. You can examine the response header to track the number of RUs that are consumed by any database operation. When you understand the factors that affect RU charges and your application's throughput requirements, you can run your application cost effectively.
<br>You provision the number of RUs for your application on a per-second basis in increments of 100 RUs per second. To scale the provisioned throughput for your application, you can increase or decrease the number of RUs at any time. You can scale in increments or decrements of 100 RUs. You can make your changes either programmatically or by using the Azure portal. You are billed on an hourly basis.
<br>You can provision throughput at two distinct granularities<br> 

-  Containers: [Provision throughput on an Azure Cosmos container](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-container-throughput)
This article explains how to provision throughput on a container (collection, graph, or table) in Azure Cosmos DB. You can provision throughput on a single container, or provision throughput on a database and share it among the containers within the database.

- Databases: [Provision throughput on an Azure Cosmos database](https://docs.microsoft.com/azure/cosmos-db/request-units)
This article explains how to provision throughput on a database in Azure Cosmos DB. You can provision throughput for a single container, or for a database and share the throughput among the containers within it.  


## **Recommended Documents**

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>With Azure Cosmos DB, you pay for the throughput you provision and the storage you consume on an hourly basis. Throughput must be provisioned to ensure that sufficient system resources are available for your Azure Cosmos database at all times. You need enough resources to meet or exceed the Azure Cosmos DB SLAs.  

[Request Unit Factors](https://docs.microsoft.com/azure/cosmos-db/request-units#request-unit-considerations)
<br>When estimating the number of RUs per second to provision, use this article to consider factors that impact RUs.  

[Optimize query cost in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/optimize-cost-queries#evaluate-request-unit-charge-for-a-query)
<br>Azure Cosmos DB offers a rich set of database operations including relational and hierarchical queries that operate on the items within a container. The cost associated with each of these operations varies based on the CPU, IO, and memory required to complete the operation. Instead of thinking about and managing hardware resources, you can think of a request unit (RU) as a single measure for the resources required to perform various database operations to serve a request. This article describes how to evaluate request unit charges for a query and optimize the query in terms of performance and cost.
