<properties
	pageTitle="Setup and Configuration/Issue using the Azure CLI or Powershell"
	description="Issue using the Azure CLI or Powershell"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="55"
	supportTopicIds="32681373"
	resourceTags=""
	productPesIds="15568"
	articleId="search-issueusingtheazurecliorpowershell"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue using the Azure CLI or Powershell

## **Recommended Steps**

Powershell and Azure CLI support the following operations for Azure Cognitive Search:
* List search services in a subscription
* Retrieve service information
* Create or delete a service
* Regenerate admin API-keys
* Create or delete query API-keys
* Scale up or down with replicas and partitions

### **Managing your search service with Powershell**

If you are new to managing Azure resources with Powershell, you should review the [Azure Powershell documentation](http://docs.microsoft.com/powershell/azure/get-started-azureps), which has a nice intro to get you started and guidance for some common operations you should be aware of.

### **Managing your search service with Azure CLI**

The easiest way to get started with the [Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli) is by running it in an Azure Cloud Shell environment through your browser. To learn about Cloud Shell, see [Quickstart for Bash in Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/quickstart). The Azure If you are new to managing Azure resources with Powershell, you should review the [Azure Powershell documentation](http://docs.microsoft.com/powershell/azure/get-started-azureps), which has a nice intro to get you started and guidance for some common operations you should be aware of.

### **Not currently supported in Powershell or Azure CLI**

Currently, you can't use Powershell or Azure CLI to change a service name, region, or migrate to a different service tier. Dedicated resources are allocated when a service is created. As such, changing the underlying infrastructure, such as Azure region or type, requires you to create a new service and reindex all of your content. There are currently no tools or APIs for transferring content, such as an index, from one service to another.

## **Recommended Documents**

* [Manage your Azure Cognitive Search service with PowerShell](https://docs.microsoft.com/azure/search/search-manage-powershell)
* [Manage your Azure Cognitive Search service with Azure CLI](https://docs.microsoft.com/cli/azure/search?view=azure-cli-latest)