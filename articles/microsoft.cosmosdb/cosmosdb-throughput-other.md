<properties
    pageTitle="Other"
    description="Other"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32741533"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-other"
    displayOrder="244"
    category="Throughput and Scaling"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Throughput and Scaling Other Topics

Most users are able to resolve their Throughput issue using the steps below. 

## **Recommended Steps**  

### **Cannot scale down RUs**  
Minimum RUs per container
* Throughput provisioned on a database: 100
* Throughput provisioned on a container: 400

There are factors that may prevent you from scaling down to the minimum as documented in [Provision throughput on containers and databases](https://docs.microsoft.com/azure/cosmos-db/set-throughput#update-throughput-on-a-database-or-a-container) such as using shared throughput.
Containers in a shared throughput database share the throughput (RU/s) allocated to that database. You can have up to four containers with a minimum of 400 RU/s on the database. Each new container after the first four will require an additional 100 RU/s minimum. For example, if you have a shared throughput database with eight containers, the minimum RU/s on the database will be 800 RU/s.  

### **RUs charge higher for inserts and deletes**
Modifying indexes would result in better performance.   
**Bulk operations using ADF?** It is expected to slow the system as bulk operation would consume most of the provisioned throughput.  It is recommended to perform such operation during less workload hours or to increase throughput for quicker data transfer.  

### **Cannot find the option to enable autoscale?** 

* You can enable autoscale on existing databases and containers through the Azure portal. 
* To create new databases and containers with autoscale, use the Azure portal, Azure Resource Manager template, or latest versions of the Azure Cosmos DB .NET SDK V3.9+ or Java SDK V4+.
* Support in Azure CLI, PowerShell, and other SDKs is planned, but not yet available.


### **I am trying to create a container programmatically cannot find the context for autoscale setting**
* You can create a new autoscale database or container using [Resource Manager templates](https://docs.microsoft.com/azure/cosmos-db/manage-sql-with-resource-manager#azure-cosmos-account-with-autoscale-throughput).
* Support for Azure CLI and PowerShell is planned, but not yet available.


### **Changing RU Throughput**
You can have several options to change the throughput for your collections or databases.  
* [Azure CLI](https://docs.microsoft.com/cli/azure/cosmosdb/collection?view=azure-cli-latest#az-cosmosdb-collection-show)
* [.NET SDK](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-database-throughput#provision-throughput-using-net-sdk)
* [Offers](https://docs.microsoft.com/rest/api/cosmos-db/offers)
* You can also change to use [autoscale throughput](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autoscale)


## **Recommended Documents**

[Use Azure Cosmos DB autoscale](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autoscale)
<br>Azure Cosmos DB allows you to set either standard (manual) or autoscale provisioned throughput on your databases and containers. This article describes the benefits and use cases of autoscale provisioned throughput.

With autoscale, Azure Cosmos DB automatically and instantly scales the throughput (RU/s) of your database or container based on usage, without impacting the availability, latency, throughput, or performance of the workload.

[How to enable autoscale](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-autoscale-throughput?tabs=api-async)
<br>You can enable autoscale on existing databases and containers through the Azure portal. To create new databases and containers with autoscale, use the Azure portal, Azure Resource Manager template, or latest versions of the Azure Cosmos DB .NET SDK V3.9+ or Java SDK V4+. See this article for samples. 

[Provision throughput on containers and databases](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
<br>An Azure Cosmos database is a unit of management for a set of containers. A database consists of a set of schema-agnostic containers. An Azure Cosmos container is the unit of scalability for both throughput and storage. A container is horizontally partitioned across a set of machines within an Azure region and is distributed across all Azure regions associated with your Azure Cosmos account.  

[How to distribute data globally with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article covers how you can configure your databases to be globally distributed and available in any of the Azure regions to lower the latency.
