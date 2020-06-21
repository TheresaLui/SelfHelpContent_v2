
<properties
	pageTitle="Troubleshoot issues connecting to Storage service over Private Endpoints"
	description="Troubleshoot issues connecting to Storage service over Private Endpoints"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689876,32689150,32689872,32689880,32689868"
	productPesIds="15629,16459,16461,16462,16598,16460"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_common_private_endpoints_connection"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot issues connecting to Storage service over Azure Private Endpoints

Azure Private Endpoint is a network interface that connects you privately and securely to a service powered by Azure Private Link. Private Endpoint uses a private IP address from your VNet, effectively bringing the Azure storage service into your VNet.

## **Recommended Steps**

Many customers resolved their Azure Private Endpoints for Storage service issues using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions.

### **Common reasons for connection failures to Storage Service with Private Endpoints**

Below are the common scenarios seen when customers reported that connections to storage services with Private Endpoints failed.

- [Only a Private Endpoint in an approved state can send traffic to storage service](https://docs.microsoft.com/azure/private-link/private-endpoint-overview#access-to-a-private-link-resource-using-approval-workflow) - If the user requesting the creation of the private endpoint is also an owner of the storage account, this consent request is automatically approved. Otherwise, the private link resource owner has to approve the private endpoint connection. Once approved the corresponding private endpoint will be enabled to send traffic to the private link resource.

- [Make sure you have appropriate DNS config in place](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#dns-changes-for-private-endpoints) - An improper DNS configuration would lead to name resolution failures

*If you're using a custom or on-premises DNS server, you should use the 'privatelink' subdomain of the storage service to configure DNS resource records for the private endpoints.*

- [Access storage account privately from the VM](https://docs.microsoft.com/azure/private-link/create-private-endpoint-storage-portal#access-storage-account-privately-from-the-vm) - DNS configuration for storage needs a manual modification on the hosts file to include the FQDN of the specific account Please modify the following file using administrator permissions on Windows: c:\Windows\System32\Drivers\etc\hosts or Linux /etc/hosts Include the DNS information for the account from previous step in the following format [Private IP Address] myaccount.blob.core.windows.net

### **Known Issues**

- [Copy Blob failures](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#copy-blob-failures)
- [Subnets with Service Endpoints](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#subnets-with-service-endpoints)
- [Storage access constraints for clients in VNets with Private Endpoints](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#storage-access-constraints-for-clients-in-vnets-with-private-endpoints)
- [Network Security Group rules for subnets with private endpoints](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#network-security-group-rules-for-subnets-with-private-endpoints)
