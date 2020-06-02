<properties
	pageTitle="Azure Synapse Link for Cosmos DB - store"
	description="Azure Synapse Link for Cosmos DB - store"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742612"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-store"
	displayOrder="302"
	category="Azure Synapse Link"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Cosmos DB Store
Most users are able to resolve their Azure Synapse Link for Cosmos DB Store issue using the steps below.  



## **Recommended Steps**  

  

### **Cannot Enable Analytical Store**
Synapse Link for the account is a prerequisite to be able to create Analytical Store enabled container

**Ensure Synapse Link is enabled for the Azure Cosmos DB account**
* Sign into the Azure Portal
* Navigate to the Azure Cosmos DB Account
* Open the Features pane
* Status of Synapse Link from the features list should say *Enrolled*

**Note:** If Status is off, you will need to enable Synapse Link for the account. You can do so directly from the Features pane in the portal or by using Azure Cosmos DB SDKs.
<br>[See instructions](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)  

**Ensure Azure Cosmos DB account is SQL API**
In public preview Synapse Link is only supported for SQL API. Support for Mongo API & Cassandra API are in gated preview. To request access email *cosmosdbsynapselink@microsoft.com* 


**Existing Containers**
Currently there is no support to enable analytical store on existing containers. You should now be able to create a new container and enable analytical store during container creation time.
<br>[See instructions](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl)  


### **Cannot Disable Analytical Store**
Currently, the analytical store cannot be disabled on an Azure Cosmos DB container after it is enabled during container creation. To stop using analytical store you will need to delete and recreate the container.  


### **Disabling Synapse Link Feature for my Azure Cosmos DB Account**
Currently, after the Synapse Link capability is enabled at the account level, youcannot disable it. If you want to turn off the capability, you must delete and recreate a new Azure Cosmos DB account.  Understand that you will not have any billing implications if the Synapse Link capability is enabled at the account level but there is no analytical store enabled containers.  


## **Recommended Documents**  

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)
<br>How-To configure and use Azure Synapse Link for Azure Cosmos DB  

[What is Azure Cosmos DB Analytical Store?](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview  

[Frequently asked questions about Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>General FAQ
