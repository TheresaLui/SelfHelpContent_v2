<properties
	pageTitle="Azure Synapse Link for Cosmos DB - How-to"
	description="Azure Synapse Link for Cosmos DB - How-to"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783706"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-howto"
	displayOrder="321"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Azure Cosmos DB - How-to 

Most users can resolve issues in Azure Synapse Link for Azure Cosmos DB by applying these answers to frequently asked questions. 


## **Recommended Steps**  

### **Supported APIs**  
Currently, Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  


### **How can I enable the analytical store?**

Synapse Link for the account is a prerequisite to be able to create the analytical store-enabled container. To make sure that Synapse Link is enabled for the Azure Cosmos DB account, do the following:

1. Sign in to the Azure portal, and navigate to the Azure Cosmos DB account.

2. Open the **Features** pane.  
   - **Note:** The status of Synapse Link from the features list should be **Enrolled**.

3. If **Status** is off, you have to enable Synapse Link for the account. You can do so directly from the **Features** pane in the portal or by using Azure Cosmos DB SDKs. See instruction here.

4. Make sure that the Azure Cosmos DB account is SQL API or MongoDB API. The analytical store for Cassandra API is in private preview. To request access, write to cosmosdbsynapselink@microsoft.com.
   - Currently, there is no support to enable analytical store on existing containers. You should be able to create a new container and enable the analytical store during container creation.
   - Currently there is no support to enable the analytical store on Azure Cosmos DB SQL serverless accounts.

### **How can I disable the analytical store?**
Currently, the analytical store cannot be disabled on an Azure Cosmos DB container after it is enabled during container creation. To stop using the analytical store, you have to delete and re-create the container.

### **How can I disable the  Synapse Link feature for my Azure Cosmos DB account?**
Currently, after the Synapse Link capability is enabled at the account level, you cannot disable it. You will not be billed if the Synapse Link capability is enabled at the account level, and there are no analytical store-enabled containers.

If you must turn off the feature, you have two options:

- Delete the Azure Cosmos DB account, and then re-create the account. If it is necessary, migrate the data.
- Open a support ticket to ask for help for a data migration to another account.

### **How can I automate Synapse Link operations?**
For help to automate Synapse LInk, go to the following resources.

#### CLI
- [Create a database account with Synapse Link enabled](https://docs.microsoft.com/cli/azure/cosmosdb?view=azure-cli-latest#az_cosmosdb_create-optional-parameters)
- [Update an existing Database account to enable Synapse Link](https://docs.microsoft.com/cli/azure/cosmosdb?iew=azure-cli-latest#az_cosmosdb_update-optional-parameters)
- [Create a MongoDB collection with the analytical store enabled](https://docs.microsoft.com/cli/azure/cosmosdb/mongodb/collection?view=azure-cli-latest#az_cosmosdb_mongodb_collection_create-examples)
- [Update a MongoDB collection analytical ttl](https://docs.microsoft.com/cli/azure/cosmosdb/mongodb/collection?view=azure-cli-latest#az_cosmosdb_mongodb_collection_update)
- [Create a SQL API container with the analytical store enabled](https://docs.microsoft.com/cli/azure/cosmosdb/sql/container?view=azure-cli-latest#az_cosmosdb_sql_container_create)
- [Update a SQL API container analytical ttl](https://docs.microsoft.com/cli/azure/cosmosdb/sql/container?view=azure-cli-latest#az_cosmosdb_sql_container_update)

#### PowerShell

- [Create a database account with Synapse Link enabled](https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount?view=azps-5.5.0#description)
- [Update an existing Database account to enable Synapse Link](https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount?view=azps-5.5.0)
- [Create a MongoDB collection with the analytical store enabled](https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection?view=azps-5.5.0#description)
- [Update a MongoDB collection analytical ttl](https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection?view=azps-5.5.0)
- [Create an SQL API container with the analytical store enabled](https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer?view=azps-5.5.0#description)
- [Update an SQL API container analytical ttl](https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer?view=azps-5.5.0)

#### SDKs

- [Create containers - Configure and use Azure Synapse Link for Azure Cosmos DB - .Net, Java, and Python SDKs](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#net-sdk)


### **Is the analytical store supported by Terraform?**  
Currently Terraform does not support the analytical store containers. See [Terraform GitHub Issues](https://github.com/hashicorp/terraform/issues) for more information.  


## **Recommended Documents**  

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)
<br>Getting started with Azure Synapse Link for Azure Cosmos DB.    

[What is Azure Cosmos DB Analytical Store?](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  

[Azure Synapse Link for Azure Cosmos DB supported features](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>This article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.   

[Azure Synapse Link for Azure Cosmos DB: Near real-time analytics use cases](https://docs.microsoft.com/azure/cosmos-db/synapse-link-use-cases)

