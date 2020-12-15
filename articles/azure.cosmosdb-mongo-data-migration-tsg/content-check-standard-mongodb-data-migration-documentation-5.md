<properties
	  pageTitle="Check standard MongoDB data migration documentation"
	  description="Check standard MongoDB data migration documentation"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="9a83ff38-aaef-4982-b3a1-acfc41355127"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check standard MongoDB data migration documentation

Customer would like to migrate their DB to another subscribtion/resource group

##Solution
The Customer can use Azure Data factory to migrate data to a new account in another subscription. Here are the instructions for copying data for the Mongo API:
https://docs.microsoft.com/en-us/azure/data-factory/connector-azure-cosmos-db-mongodb-api

Also, please review the following documentation:

- [Migrate MongoDB to Azure Cosmos DB Mongo API (offline)](https://docs.microsoft.com/en-us/azure/dms/tutorial-mongodb-cosmos-db)
- [Migrate MongoDB to Azure Cosmos DB Mongo API (online)](https://docs.microsoft.com/en-us/azure/dms/tutorial-mongodb-cosmos-db-online)

