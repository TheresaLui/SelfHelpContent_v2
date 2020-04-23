<properties
	pageTitle="Other"
	description="Other"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636814"
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

### **Cannot find the option to enable Autopilot?**  
Autopilot has been registered for all users. Autopilot can only be enabled while creating new databases and containers from the Azure Portal.
* Support for CLI and SDK is not yet available
* Support to enable autopilot mode on existing containers and databases is not yet available

### **I am trying to create the tables programmatically using ARM templates and cannot find the context for autopilot setting**
* Support for CLI and SDK is not yet available


### **Changing RU Throughput**
You can have several options to change the throughput for your collections or databases.  
* [Azure CLI](https://docs.microsoft.com/cli/azure/cosmosdb/collection?view=azure-cli-latest#az-cosmosdb-collection-show)
* [.NET SDK](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-database-throughput#provision-throughput-using-net-sdk)
* [Offers](https://docs.microsoft.com/rest/api/cosmos-db/offers)
* You can also change to use [Autopilot](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot)


## **Recommended Documents**

[Create Azure Cosmos containers and databases in autopilot mode (Preview)](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot)
<br>Azure Cosmos DB allows you to provision throughput on your containers in either manual or autopilot mode. This article describes the benefits and use cases of autopilot mode. In addition to manual provisioning of throughput, you can now configure Azure cosmos containers in autopilot mode. Azure Cosmos containers and databases configured in autopilot mode will automatically and instantly scale the provisioned throughput based on your application needs without compromising the SLAs.  

[Enable autopilot from Azure portal](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot#enable-autopilot-from-azure-portal)
<br>You can try out autopilot in your Azure Cosmos accounts by enabling in from Azure portal. Use the steps in this article to enable the autopilot option.

[Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
<br>This article explains physical and logical partitions in Azure Cosmos DB. It also discusses best practices for scaling and partitioning.  

[Provision throughput on containers and databases](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
<br>An Azure Cosmos database is a unit of management for a set of containers. A database consists of a set of schema-agnostic containers. An Azure Cosmos container is the unit of scalability for both throughput and storage. A container is horizontally partitioned across a set of machines within an Azure region and is distributed across all Azure regions associated with your Azure Cosmos account.  

[How to distribute data globally with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article covers how you can configure your databases to be globally distributed and available in any of the Azure regions to lower the latency.
