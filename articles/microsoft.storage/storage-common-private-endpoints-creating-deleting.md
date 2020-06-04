
<properties
	pageTitle="Troubleshoot issues with creating or deleting Azure Private Endpoints"
	description="Troubleshoot issues with creating or deleting Azure Private Endpoints"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689877,32689151,32689873,32689881,32689869"
	productPesIds="15629,16459,16461,16462,16598,16460"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_common_private_endpoints_creating_deleting"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot issues with creating or deleting Azure Private Endpoints

Azure Private Endpoint is a network interface that connects you privately and securely to a service powered by Azure Private Link. Private Endpoint uses a private IP address from your VNet, effectively bringing the Azure storage service into your VNet.

## **Recommended Steps**

Many customers resolved their Azure Private Endpoints for Storage service issues using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions below.

### **Creation Issues with Private Endpoints**

* [Private Endpoint](https://docs.microsoft.com/azure/private-link/private-endpoint-overview)

* [Connect privately to a storage account using Azure Private Endpoint](https://docs.microsoft.com/azure/private-link/create-private-endpoint-storage-portal)

* Create Private Endpoint
  * [Azure Portal](https://docs.microsoft.com/azure/private-link/create-private-endpoint-portal)
  * [Azure CLI](https://docs.microsoft.com/azure/private-link/create-private-endpoint-cli) 
  * [Azure PowerShell](https://docs.microsoft.com/azure/private-link/create-private-endpoint-powershell)
  

* [DNS configuration](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#dns-configuration)
  * [Configure Private DNS Zone - Azure CLI](https://docs.microsoft.com/azure/private-link/create-private-endpoint-cli#configure-the-private-dns-zone)
  * [Configure Private DNS Zone - Azure PowerShell](https://docs.microsoft.com/azure/private-link/create-private-endpoint-powershell#configure-the-private-dns-zone)

### **Known Issues**

* [Limitations of Private Endpoints](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#limitations)

