<properties
	pageTitle="Azure Synapse Link for Cosmos DB - configuration"
	description="Azure Synapse Link for Cosmos DB - configuration"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742612"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-configuration"
	displayOrder="302"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>


# Azure Synapse Link for Azure Cosmos DB - How-to 
Most users can resolve issues in Azure Synapse Link for Azure Cosmos DB by applying the following answers to frequently asked questions. 

## **Recommended Steps**  

### **Supported APIs**  
Currently, Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  

### **I cannot enable the analytical store**
If you can't enable the analytical store, verify each of the following:

- Synapse Link for the account is a prerequisite to be able to create the Analytical Store enabled container. See [Enable Azure Synapse Link for Azure Cosmos DB accounts](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#enable-synapse-link).

- Ensure that the Azure Cosmos DB account is SQL API or MongoDB API. Analytical store for Cassandra API is in private preview. To request access, email cosmosdbsynapselink@microsoft.com.  

- Currently, there is no support to enable analytical store on existing containers. You should be able to create a new container and enable analytical store during container creation time.  

- Currently there is no support to enable analytical store on Azure Cosmos DB SQL serverless accounts.  

### **How can I disable the analytical store?**
Currently, the analytical store cannot be disabled on an Azure Cosmos DB container after it is enabled during container creation. To stop using the analytical store, you need to delete and re-create the container.

### **How can I disable the  Synapse Link feature for my Azure Cosmos DB account?**
Currently, after the Synapse Link capability is enabled at the account level, you cannot disable it. You will not be billed if the Synapse Link capability is enabled at the account level, and there are no analytical store-enabled containers.

If you must turn off the feature, you have two options:

- Delete the Azure Cosmos DB account, and then re-create the account. If necessary, migrate the data.
- Open a support ticket to ask for help for a data migration to another account.

### **Configuring customer-managed keys**

#### **Which Azure Cosmos DB APIs are supported by CMK for Synapse Link?**
CMK will be applicable to APIs supported by Synapse Link: SQL API and MongoDB.  

#### **Can you set the CMK for the analytical store from the Azure portal?**
No. This feature is not available yet. At GA, we will publish ARM templates and CLI for using managed identities.  

#### **Can you revoke system identity assigned to a Cosmos DB account?**
Yes, it works like current CMK flow, using *first-party identity*. [Learn more](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-cmk). 

#### **Error: First-party identity is not supported for analytics account.**
This error message is returned when a user enables Synapse Link, and the `defaultidentity` value is not set to `UseSystemAssigned`. This message is also returned when a customer sets `defaultIdentity` to `UseFirstPartyIdentity` after turning on CMK + Synapse Link.

#### **Error: Cosmos DB will treat the keys as "revoked" in following scenarios.**
If the user removes first-party identity from Azure Key vault + adds a system identity, without setting the `identity type` to `UseSystemAssigned`.  

### **If you add first-party identity to Azure Key vault + system identity, removes first-party identity, revokes system identity**
To recover: Specify the correct identity in the Azure Key vault access policy again. Cosmos DB will automatically detect this change and recover.

### **If you delete the system identity for an Azure Cosmos DB account and Cosmos DB account is set to "DefaultIdentity"=="UseSystemAssigned"**
Cosmos DB will treat the keys as "revoked" and set the "DefaultIdentity"=="None".  

To recover: Create a new system identity for the Azure Cosmos DB account. Specify this identity in AKV access policy and reset "DefaultIdentity" to "UseSystemAssigned".

### **Is analytical store supported by Terraform?**
Currently, Terraform doesn't support analytical store containers. [Learn more](https://github.com/hashicorp/terraform/issues).  

### **How can I automate Synapse Link operations?**
For help to automate Synapse LInk, go to the resources listed below.

#### CLI
- [Create a database account with Synapse Link enabled](https://docs.microsoft.com/cli/azure/cosmosdb?view=azure-cli-latest#az_cosmosdb_create-optional-parameters)
- [Update an existing database account to enable Synapse Link](https://docs.microsoft.com/cli/azure/cosmosdb?iew=azure-cli-latest#az_cosmosdb_update-optional-parameters)
- [Create a MongoDB collection with analytical store enabled](https://docs.microsoft.com/cli/azure/cosmosdb/mongodb/collection?view=azure-cli-latest#az_cosmosdb_mongodb_collection_create-examples)
- [Update a MongoDB collection analytical ttl](https://docs.microsoft.com/cli/azure/cosmosdb/mongodb/collection?view=azure-cli-latest#az_cosmosdb_mongodb_collection_update)
- [Create a SQL API container with analytical store enabled](https://docs.microsoft.com/cli/azure/cosmosdb/sql/container?view=azure-cli-latest#az_cosmosdb_sql_container_create)
- [Update a SQL API container analytical ttl](https://docs.microsoft.com/cli/azure/cosmosdb/sql/container?view=azure-cli-latest#az_cosmosdb_sql_container_update)

#### PowerShell

- [Create a database account with Synapse Link enabled](https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount?view=azps-5.5.0#description)
- [Update an existing Database account to enable Synapse Link](https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount?view=azps-5.5.0)
- [Create a MongoDB collection with analytical store enabled](https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection?view=azps-5.5.0#description)
- [Update a MongoDB collection analytical ttl](https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection?view=azps-5.5.0)
- [Create an SQL API container with analytical store enabled](https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer?view=azps-5.5.0#description)
- [Update an SQL API container analytical ttl](https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer?view=azps-5.5.0)

#### SDKs  
- [Create containers - Configure and use Azure Synapse Link for Azure Cosmos DB - .Net, Java, and Python SDKs](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#net-sdk)

## **Recommended Documents**  

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)

[What is Azure Cosmos DB Analytical Store?](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB  

[Azure Synapse Link for Azure Cosmos DB supported features](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>Functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB   

[Azure Synapse Link for Azure Cosmos DB: Near real-time analytics use cases](https://docs.microsoft.com/azure/cosmos-db/synapse-link-use-cases)

