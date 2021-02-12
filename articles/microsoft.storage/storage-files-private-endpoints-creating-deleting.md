
<properties
	pageTitle="Troubleshoot issues with creating or deleting Azure Private Endpoints"
	description="Troubleshoot issues with creating or deleting Azure Private Endpoints"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="kartikshah9"
	ms.author="kashah"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689869"
	productPesIds="16460"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_files_private_endpoints_creating_deleting"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Troubleshoot issues with creating or deleting Azure Private Endpoints

Azure Private Endpoint is a network interface that connects you privately and securely to a service powered by Azure Private Link. Private Endpoint uses a private IP address from your VNet, effectively bringing the Azure storage service into your VNet.

## **Recommended Steps**

Many customers resolved their Azure Private Endpoints for Storage service issues using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions below.

### **Azure Files and Private Endpoints**

- [Overview on Private Endpoints for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-files-networking-overview#private-endpoints)
- [Step by step instructions to setup Private Endpoints for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-files-networking-endpoints?tabs=azure-portal#create-a-private-endpoint)

### **Azure File Sync and Private Endpoints**

- [Overview on Private Endpoints for Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-networking-overview#private-endpoints)
- [Step by step instructions to setup Private Endpoints for Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-networking-endpoints?tabs=azure-portal)


### **Creation Issues with Private Endpoints**

* [Private Endpoint](https://docs.microsoft.com/azure/private-link/private-endpoint-overview)
* [Connect privately to a storage account using Azure Private Endpoint](https://docs.microsoft.com/azure/private-link/create-private-endpoint-storage-portal)

* Create Private Endpoint
  * [Azure Portal](https://docs.microsoft.com/azure/private-link/create-private-endpoint-portal)
  * [Azure CLI](https://docs.microsoft.com/azure/private-link/create-private-endpoint-cli) 
  * [Azure PowerShell](https://docs.microsoft.com/azure/private-link/create-private-endpoint-powershell)
  


