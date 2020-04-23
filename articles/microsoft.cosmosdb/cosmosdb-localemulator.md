<properties
	pageTitle="Cosmos DB Emulator"
	description="Cosmos DB Emulator"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32675642"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-localemulator"
	displayOrder="127"
	category="Tools and Connectors"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Emulator
Most users are able to resolve their Cosmos DB Emulator issue using the steps below.

## **Recommended Steps**

The Azure Cosmos DB Emulator provides a local environment that emulates the Azure Cosmos DB service for development purposes.
By using the Azure Cosmos DB Emulator, you can develop and test your application locally, without creating an Azure subscription or incurring any costs.

* If you installed a new version of the Emulator and are experiencing connectivity errors, ensure you reset your data. You can reset your data by right-clicking the Azure Cosmos DB Emulator icon on the system tray, and then clicking 'Reset Data'. If that does not fix the errors, you can uninstall and reinstall the app.
* If you experience crashes in CosmosDB.StartupEntryPoint.exe, run the following command from an admin command prompt: `lodctr /R`
* If you receive a Service Unavailable message, the emulator might have failed to initialize the network stack. Check to see if you have the Pulse secure client or Juniper networks client installed. The network filter drivers of these clients may cause issues. Uninstalling third-party network filter drivers typically fixes the issue.
* Collect trace files and attach them to the support case for crashes or connectivity issues 

## **Recommended Documents**

[Download MSI](https://docs.microsoft.com/azure/cosmos-db/local-emulator#installation)
<br> Download the emulator  

[Docker Hub link](https://hub.docker.com/r/microsoft/azure-cosmosdb-emulator)
<br>his repository contains the Azure Cosmos Emulator installed and prepared.   

[Docker source on Github](https://github.com/Azure/azure-cosmos-db-emulator-docker)
<br>Contains Dockerfiles for the Azure Cosmos DB Emulator.  

[Azure Cosmos DB Emulator](https://docs.microsoft.com/azure/cosmos-db/local-emulator)
<br>The Azure Cosmos Emulator provides a local environment that emulates the Azure Cosmos DB service for development purposes. Using the Azure Cosmos Emulator, you can develop and test your application locally, without creating an Azure subscription or incurring any costs. When you're satisfied with how your application is working in the Azure Cosmos Emulator, you can switch to using an Azure Cosmos account in the cloud.  




