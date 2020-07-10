<properties
	pageTitle="Azure Cosmos DB Cassandra authentication"
	description="Troubleshoot Azure Cosmos DB Cassandra authentication issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636769"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-authentication"
	displayOrder="140"
	category="Cassandra"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Cassandra authentication

Most users are able to resolve their Cosmos DB Cassandra authentication using the steps below. 

## **Recommended Steps**

To resolve this issue, try the following methods:

* Validate that the connection string specified in your application matches with the Azure Cosmos DB connection string retrieved from the Connection string tab of the Azure Portal.
* Review the secret key and remove any spaces at the start or at the end of the string.
* Ensure that SSL is enabled in the connection options.


## **Recommended Documents**

[Securing access to Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data)
<br>This article provides an overview of securing access to data stored in Microsoft Azure Cosmos DB.  

[Access Control on Azure Cosmos DB Resources](https://docs.microsoft.com/rest/api/cosmos-db/access-control-on-cosmosdb-resources)
<br>This article covers the SQL API for Azure Cosmos DB. Access to resources in the SQL API is governed by a master key token or a resource token. To access a resource, the selected token is included in the REST authorization header, as part of the authorization string.  

[Azure Cosmos DB database security](https://docs.microsoft.com/azure/cosmos-db/database-security)
<br>This article discusses database security best practices and key features offered by Azure Cosmos DB to help you prevent, detect, and respond to database breaches.
