
<properties
	pageTitle="Troubleshoot consent approval/rejection with Azure Private Endpoints for Storage service"
	description="Troubleshoot consent approval/rejection with Azure Private Endpoints for Storage service"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689875,32689149,32689871,32689879,32689867"
	productPesIds="15629,16459,16461,16462,16598,16460"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_common_private_endpoints_consent_request"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot consent approval/rejection with Azure Private Endpoints for Storage service

Azure Private Endpoint is a network interface that connects you privately and securely to a service powered by Azure Private Link. Private Endpoint uses a private IP address from your VNet, effectively bringing the Azure storage service into your VNet.

## **Recommended Steps**

Many customers resolved their Azure Private Endpoints for Storage service issues using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions below.

### **Approval and Rejection Issues with Private Endpoints**

When you create a private endpoint for a storage service in your VNet, a consent request is sent for approval to the storage account owner.

* [User requesting is owner or has permission on the account](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow) - If the user requesting the creation of the private endpoint is also an owner of the storage account, this consent request is automatically approved.
* [User requesting is not the owner or doesn't have permission on the account](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow) - An approval workflow will be initiated. The private endpoint and subsequent private endpoint connection will be created in a "Pending" state. The private link resource owner is responsible to approve the connection. After it's approved, the private endpoint is enabled to send traffic normally, as shown in the approval workflow diagram in this [article](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow).

### **Manage Private Endpoint Connections**

* [Manage a Private Endpoint connection](https://docs.microsoft.com/azure/private-link/manage-private-endpoint)
* [Manage Private Endpoint Connections on Azure PaaS resources](https://docs.microsoft.com/azure/private-link/manage-private-endpoint#manage-private-endpoint-connections-on-azure-paas-resources)

### **Known Issues**

* [Copy Blob failures](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#copy-blob-failures)
* [Subnets with Service Endpoints](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#subnets-with-service-endpoints)
* [Storage access constraints for clients in VNets with Private Endpoints](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#storage-access-constraints-for-clients-in-vnets-with-private-endpoints)
* [Network Security Group rules for subnets with private endpoints](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#network-security-group-rules-for-subnets-with-private-endpoints)
