<properties
	pageTitle="Limits in Azure Cosmos DB" 
	description="Limits in Azure Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636797"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-limits-quotas"
	displayOrder="200"
	category="Limits and quotas"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Limits in Azure Cosmos DB

The below recommended document provides an overview of the limits in the Azure Cosmos DB service. Most users are able to resolve their Limits case using the steps below.

## **Recommended Steps**

Look for the specific limit or quota threshold and the appropriate way to raise the limit if needed. 

### **Document size cannot exceed 2 MB**  
Cosmos DB has a per document size limit of 2MB [Azure Cosmos DB Per-item limits.](https://docs.microsoft.com/azure/cosmos-db/concepts-limits#per-item-limits)  
**Solution:** If your requirements need to exceed this, it is recommended to split the document into multiple sub-documents and create a new field to link them together.  When retrieving, you would use a query to retrieve all documents that are linked together.  





## **Recommended Documents**

[Limits in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/concepts-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[Create Azure Cosmos containers and databases in autopilot mode (Preview)](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot)
<br>Azure Cosmos DB allows you to provision throughput on your containers in either manual or autopilot mode. This article describes the benefits and use cases of autopilot mode. In addition to manual provisioning of throughput, you can now configure Azure cosmos containers in autopilot mode. Azure Cosmos containers and databases configured in autopilot mode will automatically and instantly scale the provisioned throughput based on your application needs without compromising the SLAs.  

[Request Unit Factors](https://docs.microsoft.com/azure/cosmos-db/request-units#request-unit-considerations)
<br>When estimating the number of RUs per second to provision, use this article to consider factors that impact RUs.  

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>With Azure Cosmos DB, you pay for the throughput you provision and the storage you consume on an hourly basis. Throughput must be provisioned to ensure that sufficient system resources are available for your Azure Cosmos database at all times. You need enough resources to meet or exceed the Azure Cosmos DB SLAs.  

