<properties
	pageTitle="Connectivity"
	description="Troubleshoot Azure Cosmos DB Connectivity issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="markjbrown"
	ms.author="mjbrown"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="cosmosdb-connectivity-mooncake"
	displayOrder="22"
	category="Core (SQL)"
/>

# Connectivity in Azure Cosmos DB

You may get connectivity errors due to client, server, or environment (network) issues. If you see no Azure Cosmos DB service advisory error messages in the [Azure Service Health portal](https://www.azure.cn/home/features/service-health/), it may be due to a network issue or high resource contention on the client machine e.g. high CPU, network exhaustion, or high memory utilization.

## **Recommended Steps**

### **Single machine cannot connect**

If the Cosmos DB account you are connecting to has an [IP firewall](https://docs.azure.cn/cosmos-db/firewall-support) then only the allowed list of client IPs will be able to connect to it. If just one of your machine having connectivity issues to the Cosmos DB account, then, this might be one of the reasons impacting connectivity. Follow the tips in the below documentation links to avoid or correct this issue.

* [How to configure IP firewall in Azure Cosmos DB](https://docs.azure.cn/cosmos-db/how-to-configure-firewall)

### **Multiple machines cannot connect**

If the Cosmos DB account you are connecting to is configured to only allow access from within a Virtual Network, then only machines configured for access through allowed Virtual Network subnets will be allowed. Follow the tips in the below documentation links to determine connectivity issues and correct.

* [Connection troubleshooting with Azure Network Monitoring](https://docs.azure.cn/network-watcher/network-watcher-connectivity-overview)
* [Diagnose outbound connections from a VM](https://docs.azure.cn//network-watcher/network-watcher-monitoring-overview#connection-troubleshoot)
* [Configure access to Azure Cosmos DB from Virtual Networks](https://docs.azure.cn/cosmos-db/how-to-configure-vnet-service-endpoint)

## **Recommended Documents**

* [Connection mode](https://docs.azure.cn/cosmos-db/performance-tips#networking)
* [SDK usage](https://docs.azure.cn/cosmos-db/performance-tips#sdk-usage)
* [Azure Cosmos DB firewall support](https://docs.azure.cn/cosmos-db/firewall-support)
