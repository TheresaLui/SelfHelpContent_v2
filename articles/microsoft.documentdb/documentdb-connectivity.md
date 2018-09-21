<properties
	pageTitle="Connectivity"
  	description="Conectivity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	displayOrder="103"
	selfHelpType="resource"
	supportTopicIds="32597503"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Connectivity in Azure Cosmos DB

You may get connectivity errors due to client, server, or environment (network) issues. If you see no Azure Cosmos DB service advisory error message, it's most likely due to a network issue or high resource contention on the client machine e.g. high CPU, network exhaustion, or high memory utilization. Also, if the Cosmos DB account you are connecting to has an IP policy-based access control setup, only allowed list of client IPs will be able to connect to it, so if just one of your machine is having connectivity issues to the Cosmos DB account this might be one of the reasons. Follow the tips in the below documentation links to avoid such issues.

## **Recommended documents**

* [Connection mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* [SDK usage](https://docs.microsoft.com/azure/cosmos-db/performance-tips#sdk-usage)
* [Azure Cosmos DB firewall support](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
