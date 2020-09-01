<properties
	pageTitle="Connectivity"
	description="Troubleshoot Azure Cosmos DB Connectivity issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636777,32692541"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-connectivity"
	displayOrder="62"
	category="Core (SQL)"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Connectivity in Azure Cosmos DB  
You may get connectivity errors due to client, server, or environment (network) issues. If you see no Azure Cosmos DB service advisory error messages in the [Azure Service Health portal](https://azure.microsoft.com/features/service-health/), it may be due to a network issue or high resource contention on the client machine e.g. high CPU, network exhaustion, or high memory utilization.

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**
* Always ensure you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet).
* Ensure you are using singleton client.  

### **Multiple machines cannot connect**  
If the Cosmos DB account you are connecting to is configured to only allow access from within a Virtual Network, then only machines configured for access through allowed Virtual Network subnets will be allowed.  
Follow the tips in the below documentation links to determine connectivity issues and correct:
* [Connection troubleshooting with Azure Network Monitoring](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-overview) 
* [Diagnose outbound connections from a VM](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview#connection-troubleshoot)
* [Configure access to Azure Cosmos DB from Virtual Networks](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)

## **Recommended Documents**  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  

[How to configure IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
<br>Learn how you can set an IP firewall on the Azure Cosmos DB account using the following:
* From the Azure portal
* Declaratively by using an Azure Resource Manager template
* Programmatically through the Azure CLI or Azure PowerShell by updating the ipRangeFilter property  

[Frequently Asked Questions: How to configure access from virtual networks (VNet)](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
<br>This article describes how to configure a virtual network service endpoint for an Azure Cosmos DB account, and provides answers to frequently asked questions.  

[IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
<br>This article provides an IP access control overview.
