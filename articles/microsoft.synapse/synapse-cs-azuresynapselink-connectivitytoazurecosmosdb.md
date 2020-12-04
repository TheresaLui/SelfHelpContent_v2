<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783844"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Azure Synapse Link/Connectivity to Azure Cosmos DB"
    description = "Azure Synapse Link/Connectivity to Azure Cosmos DB"
    articleId = "synapse-cs-azuresynapselink-connectivitytoazurecosmosdb.md"
    ms.author = "saltug"
/>

# Azure Synapse Link/Connectivity to Azure Cosmos DB

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using the steps below.  

## **Recommended Steps**  

### **Supported APIs**  

Today Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview, for more information please contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  

### **Workspace with Managed Virtual Network**   
Azure Synapse Link for Azure Cosmos DB is currently not supported in workspace with Managed Vnet.   

We recommend creating a workspace without Managed Vnet to access Azure Synapse Link.  


### **Cannot access Cosmos DB analytical store with Synapse SQL dedicated pool**  
Only Synapse SQL serverless pool and Synapse Spark pool are currently supported. Synapse SQL dedicated pool is not supported.  

## **Recommended Documents**  

[Azure Synapse Link limits](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>This article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.
 