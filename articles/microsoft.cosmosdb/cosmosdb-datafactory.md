<properties
	pageTitle="Azure Data Factory connector"
	description="Troubleshoot Azure Cosmos DB Azure Data Factory connector"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636781"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-datafactory"
	displayOrder="122"
	category="Tools and Connectors"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Data Factory connector  
Most users are able to resolve their Cosmos DB related Data Factory issue using the steps below.

## **Recommended Steps**  


### **Copy Data from Cosmos Db to Storage Account**  
**Issue**  
 Not able to configure the subnets on the Storage Account Firewall settings.

**Solution**  
To apply a virtual network rule to a storage account, the user must have the appropriate permissions for the subnets being added. The permission needed is Join Service to a Subnet and is included in the Storage Account Contributor built-in role. It can also be added to custom role definitions.






## **Recommended Documents**
[Copy data to or from Azure Cosmos DB (SQL API) by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db)
<br>This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB (SQL API), and use Data Flow to transform data in Azure Cosmos DB (SQL API).   

[Copy data to or from Azure Cosmos DB's API for MongoDB by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)
<br>This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB's API for MongoDB. 