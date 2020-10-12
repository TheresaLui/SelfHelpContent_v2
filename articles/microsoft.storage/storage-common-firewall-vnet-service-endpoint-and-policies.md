
<properties
	pageTitle="Troubleshoot and resolve Azure Storage Firewall & VNet issues with Service Endpoint"
	description="Troubleshoot and resolve Azure Storage Firewall & VNet issues with Service Endpoint"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32682430,32682435,32682440,32682445"
	productPesIds="15629,16459,16461,16462,16598"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_common_firewall_vnet_service_endpoint_and_policies"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot and resolve VNet Service Endpoint issue with Azure Storage

Most customers resolved their VNet service endpoint issue with Azure storage by referring the articles below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions.

## **Recommended Steps**

Services running inside a VNet with service endpoint policy must add the storage account explicitly in the policy.
Refer below to make the necessary changes:

1. [Virtual network service endpoint policies](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview)
2. [Configure VNet endpoint policies for Azure Storage](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#configuration)
3. [Limitations of VNet endpoint policies](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#limitations)
4. [Logging and troubleshooting](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#logging-and-troubleshooting)
