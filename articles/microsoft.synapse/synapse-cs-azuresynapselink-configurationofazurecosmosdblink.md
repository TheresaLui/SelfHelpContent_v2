<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783843"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Azure Synapse Link/Configuration of Azure Cosmos DB link"
    description = "Azure Synapse Link/Configuration of Azure Cosmos DB link"
    articleId = "synapse-cs-azuresynapselink-configurationofazurecosmosdblink.md"
    ms.author = "saltug"
/>

# Azure Synapse Link/Configuration of Azure Cosmos DB link

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using the steps below.  

## **Recommended Steps**  

### **Supported APIs**  

Currently, Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  

### **Cannot enable Analytical Store**


**1.** Synapse Link for the account is a prerequisite to be able to create the Analytical Store enabled container. To ensure that Synapse Link is enabled for the Azure Cosmos DB account, do the following:

- Sign in to the Azure Portal, then navigate to the Azure Cosmos DB Account. Open the Features pane. The status of Synapse Link from the features list should be Enrolled
- If Status is off, you will need to enable Synapse Link for the account. You can do so directly from the Features pane in the portal or by using Azure Cosmos DB SDKs. See instruction here


**2.** Ensure that the Azure Cosmos DB account is SQL API or Mongo DB API. Analytical store for Cassandra API is in private preview. To request access, email cosmosdbsynapselink@microsoft.com.  


**3.** Currently there is no support to enable analytical store on existing containers. You should be able to create a new container and enable analytical store during container creation time.  


**4.** Currently there is no support to enable analytical store on Azure Cosmos DB SQL serverless accounts.  


### **Unable to disable Analytical Store**  

Currently, the analytical store cannot be disabled on an Azure Cosmos DB container after it is enabled during container creation. To stop using analytical store, you will need to delete and recreate the container.  

### **Disabling Synapse Link feature for my Azure Cosmos DB account**  

Currently, after the Synapse Link capability is enabled at the account level, you cannot disable it. You will not be billed if the Synapse Link capability is enabled at the account level and there are no analytical store enabled containers. 

If you need to turn off the capability, you have two options. You can delete and recreate a new Azure Cosmos DB account, migrating the data if necessary. Or you can open a support ticket and ask for help on a data migration to another account.

## **Recommended Documents**

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)
<br>How-To configure and use Azure Synapse Link for Azure Cosmos DB

[What is Azure Cosmos DB Analytical Store](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB
 