<properties
	pageTitle="Connectivity"
	description="Connectivity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="generic"
	supportTopicIds="32636777"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="2656f397-3f16-4a3f-bd2e-b8552509e265"
/>

# Connectivity in Azure Cosmos DB

You may get connectivity errors due to client, server, or environment (network) issues. If you see no Azure Cosmos DB service advisory error message, it's most likely due to a network issue or high resource contention on the client machine e.g. high CPU, network exhaustion, or high memory utilization. 

Also, if the Cosmos DB account you are connecting to has an IP policy-based access control setup, then, only allowed list of client IPs will be able to connect to it. If just one of your machine having connectivity issues to the Cosmos DB account, then, this might be one of the reasons impacting connectivity. Follow the tips in the below documentation links to avoid such issues:

## **Recommended documents**

* [Connection mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* [SDK usage](https://docs.microsoft.com/azure/cosmos-db/performance-tips#sdk-usage)
* [Azure Cosmos DB firewall support](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
