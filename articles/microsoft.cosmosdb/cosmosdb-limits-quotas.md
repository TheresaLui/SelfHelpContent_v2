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
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-limits-quotas"
    displayOrder="200"
    category="Limits and quotas"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Limits in Azure Cosmos DB

The below recommended document provides an overview of the limits in the Azure Cosmos DB service. Most users are able to resolve their Limits case using the steps below.

## **Recommended Steps**

### **Document size cannot exceed 2 MB**  
Cosmos DB has a per document size limit of 2MB [Azure Cosmos DB Per-item limits.](https://docs.microsoft.com/azure/cosmos-db/concepts-limits#per-item-limits)  
**Solution:** If your requirements need to exceed this, it is recommended to split the document into multiple sub-documents and create a new field to link them together.  When retrieving, you would use a query to retrieve all documents that are linked together.  

## **Recommended Documents**

[Limits in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/concepts-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[How to enable autoscale on a database or container](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-autoscale-throughput?tabs=api-async)
<br> Autoscale automatically scales the RU/s of your database or container between the max RU/s you set, and 0.1 * max RU/s. 

You can enable autoscale on existing resources through the Azure portal. To create new autoscale resources, use an Azure Resource Manager template or the latest versions of the Azure Cosmos DB .NET SDK V3.9+ and Java SDK V4+. See this article for samples. 


[Request Unit Factors](https://docs.microsoft.com/azure/cosmos-db/request-units#request-unit-considerations)
<br>When estimating the number of RUs per second to provision, use this article to consider factors that impact RUs.  

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>With Azure Cosmos DB, you pay for the throughput you provision and the storage you consume on an hourly basis. Throughput must be provisioned to ensure that sufficient system resources are available for your Azure Cosmos database at all times. You need enough resources to meet or exceed the Azure Cosmos DB SLAs.  

