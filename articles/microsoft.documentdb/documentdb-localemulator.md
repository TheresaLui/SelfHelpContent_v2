<properties
	pageTitle="Cosmos DB Emulator"
	description="Cosmos DB Emulator"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="91"
	selfHelpType="resource"
	supportTopicIds="32597531"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Azure Cosmos DB Emulator

## **Recommended Steps**

The Azure Cosmos DB Emulator provides a local environment that emulates the Azure Cosmos DB service for development purposes.
By using the Azure Cosmos DB Emulator, you can develop and test your application locally, without creating an Azure subscription or incurring any costs.

### **Troubleshooting**

* If you installed a new version of the Emulator and are experiencing connectivity errors, ensure you reset your data. You can reset your data by right-clicking the Azure Cosmos DB Emulator icon on the system tray, and then clicking 'Reset Data'. If that does not fix the errors, you can uninstall and reinstall the app.
* If you experience crashes in CosmosDB.StartupEntryPoint.exe, run the following command from an admin command prompt: lodctr /R
* If you receive a Service Unavailable message, the emulator might have failed to initialize the network stack. Check to see if you have the Pulse secure client or Juniper networks client installed. The network filter drivers of these clients may cause issues. Uninstalling third-party network filter drivers typically fixes the issue.
* Collect trace files and attach them to the support case for crashes or connectivity issues 

## **Recommended Documents**

* [Azure Cosmos DB Emulator](https://docs.microsoft.com/azure/cosmos-db/local-emulator)
* [Download MSI](https://aka.ms/cosmosdb-emulator)
* [Docker Hub link](https://hub.docker.com/r/microsoft/azure-cosmosdb-emulator)
* [Docker source on Github](https://github.com/Azure/azure-cosmos-db-emulator-docker)
