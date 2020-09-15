
<properties
	pageTitle="Troubleshoot consent approval/rejection with Azure Private Endpoints for Storage service"
	description="Troubleshoot consent approval/rejection with Azure Private Endpoints for Storage service"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="kartikshah9"
	ms.author="kashah9"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689867"
	productPesIds="16460"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_files_private_endpoints_consent_request"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Troubleshoot consent approval/rejection with Azure Private Endpoints for Storage service

Azure Private Endpoint is a network interface that connects you privately and securely to a service powered by Azure Private Link. Private Endpoint uses a private IP address from your VNet, effectively bringing the Azure storage service into your VNet.

## **Recommended Steps**

Many customers resolved their Azure Private Endpoints for Storage service issues using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions below.


### **Azure Files and Private Endpoints**

- [Overview on Private Endpoints for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-files-networking-overview#private-endpoints)
- [Step by step instructions to setup Private Endpoints for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-files-networking-endpoints?tabs=azure-portal#create-a-private-endpoint)

### **Azure File Sync and Private Endpoints**

- [Overview on Private Endpoints for Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-networking-overview#private-endpoints)
- [Step by step instructions to setup Private Endpoints for Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-networking-endpoints?tabs=azure-portal)


### **Approval and Rejection Issues with Private Endpoints**

When you create a private endpoint for a storage service in your VNet, a consent request is sent for approval to the storage account owner.

* [User requesting is owner or has permission on the account](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow) - If the user requesting the creation of the private endpoint is also an owner of the storage account, this consent request is automatically approved.
* [User requesting is not the owner or doesn't have permission on the account](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow) - An approval workflow will be initiated. The private endpoint and subsequent private endpoint connection will be created in a "Pending" state. The private link resource owner is responsible to approve the connection. After it's approved, the private endpoint is enabled to send traffic normally, as shown in the approval workflow diagram in this [article](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow)

