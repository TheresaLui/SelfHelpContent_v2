<properties
	pageTitle="Deploy Cosmos DB from Azure CLI & PowerShell" 
	description="Deploy Cosmos DB from Azure CLI & PowerShell"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balakrishnanshankar"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32597494"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"/>
	
# Unable to create collection with Unique Key from CLI

The Azure Cli does not have option to create collection with Unique Key yet.  We would be enchacing the cli command to include 
the Unique Key option in coming months.  However, for now you can use the Cosmos DB SDKs to create the collection with Unique Key. 
You can refer Collection Creation Sample(https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample)


## **Recommended documents**



# Could not find command-lets to create cosmos db collection in Powerhshell

The Azure Cosmos DB Powershell does not have command-lets to manage the runtime resource such as Database, Collection/Tables/graphs, Users, Permissions, documents/items/nodes/edges and attachments 

You can use the below approaches to manage the runtime resources.

* Using the C# Console Application



