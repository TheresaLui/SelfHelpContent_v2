<properties
	pageTitle="IP filter"
  	description="Troubleshoot CosmosDB firewall connectivity issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32636792,32675639"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-ipfilter"
	displayOrder="25"
	category="Administration"
/>

# Connecting to Azure Cosmos DB accounts  


## **Recommended Steps**
**Review VNet Frequently asked questions**
[Review frequently asked questions about configuring access from virtual networks](https://docs.microsoft.com/azure/cosmos-db/vnet-service-endpoint)  

**Can't access your Cosmos DB account from the Azure Portal**
<br>
- If you can't access your Cosmos DB account from the Azure Portal after enabling IP firewall or adding your account to a virtual network, make sure to tick the "Allow access from Azure Portal" checkbox on the "Firewall and virtual networks" section  
<br>
![throughput visual](https://docs.microsoft.com/azure/cosmos-db/media/how-to-configure-firewall/enable-azure-portal.png)  

**The Option 'Accept connection from within public Azure datacenters' becomes un-selected**
<br>
[Cosmos DB Article: Allow requests from global Azure datacenters or other sources within Azure](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall#allow-requests-from-global-azure-datacenters-or-other-sources-within-azure)
* The 0.0.0.0 address restricts requests to your Azure Cosmos DB account from Azure datacenter IP range. This setting does not allow access for any other IP ranges to your Azure Cosmos DB account.  Remove the 0.0.0.0 address.  



**If you are having connectivity issues with your Cosmos DB account with IP firewall enabled**
<br>
- You may have not added your IP address or IP address ranges in your account's firewall and virtual networks settings. To configure IP policy-based access control, you must provide the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account. Note that changes in firewall rules can take up to 15 minutes to apply.
<br>
- If you want to extend access to any Azure service, tick the "Accept connections from within public Azure datacenters" checkbox on the "Firewall and virtual networks" section  


**If you are having connectivity issues while accessing Cosmos DB through a virtual network (VNet)**
<br>
When using subnets, you have to
- Enable [Service Endpoints](https://docs.microsoft.com/azure/cosmos-db/vnet-service-endpoint) on the subnet
<br>
- Make sure that the apps or services trying to connect to your Cosmos DB instance sit in the same virtual network and subnet as the Cosmos DB instance  

If you want to extend access to any Azure service that's not part of the virtual network, tick the "Accept connections from within public Azure datacenters" checkbox on the "Firewall and virtual networks" section.  

**Can I "Accept connections from within public Azure datacenters" when service endpoint access is enabled for Azure Cosmos DB?**
<br>
- This is required only when you want your Azure Cosmos DB account to be accessed by other Azure first party services like Azure Data factory, Azure Cognitive Search or any service that is deployed in given Azure region.  


##

## **Recommended Documents**

* [How to configure IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
<br>
Learn how you can set an IP firewall on the Azure Cosmos DB account using the following
- From the Azure portal
- Declaratively by using an Azure Resource Manager template
- Programmatically through the Azure CLI or Azure PowerShell by updating the ipRangeFilter property


* [Frequently Asked Questions: How to configure access from virtual networks (VNet)](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
<br>
This article describes how to configure a virtual network service endpoint for an Azure Cosmos DB account, and provides answers to frequently asked questions.


* [IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
<br>
This article provides an IP access control overview
