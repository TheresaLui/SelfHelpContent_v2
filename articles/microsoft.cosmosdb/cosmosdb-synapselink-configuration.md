<properties
	pageTitle="Azure Synapse Link for Cosmos DB - configuration"
	description="Azure Synapse Link for Cosmos DB - configuration"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742612,32743054"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-configuration"
	displayOrder="302"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>


# Azure Synapse Link for Cosmos DB - Configuration
Most users are able to resolve their Azure Synapse Link for Cosmos DB Configuration issue using the steps below.  


## **Recommended Steps**   

### **Cannot enable Analytical Store**
**1.** Synapse Link for the account is a prerequisite to be able to create Analytical Store enabled container.

Ensure Synapse Link is enabled for the Azure Cosmos DB account by
- Signing into the Azure Portal->Navigate to the Azure Cosmos DB Account->Open Features pane->Status of Synapse Link from the features list should say Enrolled

- If Status is off, you will need to enable Synapse Link for the account. You can do so directly from the Features pane in the portal or by using Azure Cosmos DB SDKs. See instruction here

**2.** Ensure Azure Cosmos DB account is SQL API. In public preview Synapse Link is only supported for SQL API. Support for Mongo API & Cassandra API are in gated preview. To request access email *cosmosdbsynapselink@microsoft.com*.  

**3.** Currently there is no support to enable analytical store on existing containers. You should now be able to create a new container and enable analytical store during container creation time.

<br>

### **Unable to disable Analytical Store**  
Currently, the analytical store cannot be disabled on an Azure Cosmos DB container after it is enabled during container creation. To stop using analytical store you will need to delete and recreate the container.  

<br>

### **Disabling Synapse Link feature for my Azure Cosmos DB account**  
Currently, after the Synapse Link capability is enabled at the account level, you cannot disable it.  
If you want to turn off the capability, you must delete and recreate a new Azure Cosmos DB account. Understand that you will not have any billing implications if the Synapse Link capability is enabled at the account level and there is no analytical store enabled containers.

<br>

### **Cannot access Cosmos DB analytical store with Synapse SQL Serverless**
Synapse SQL Serverless is currently under gated preview and not publicly available. To request access please email *cosmosdbsynapselink@microsoft.com*.   

<br>



## Recommended Documents 

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)
<br>How-To configure and use Azure Synapse Link for Azure Cosmos DB.    

[What is Azure Cosmos DB Analytical Store](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  
