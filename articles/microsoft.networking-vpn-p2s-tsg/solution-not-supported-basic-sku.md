<properties
	pageTitle="Basic SKU does not support this scenario"
	description="Basic SKU does not support this scenario"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="bdc17bb5-946c-4bf3-b52f-d37b21e85fdd"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Basic SKU does not support this scenario

We found that this is not a supported scenario for Basic SKU VPN gateways or 'Classic' gateways. Basic gateways must be resized to Standard SKU or greater. Classic gateways must have the vnet and all resources migrated to Azure Resource Management (ARM) resources.

## Recommended Steps

1. For Basic SKU gateways, resize to Standard SKU or greater
2. For 'Classic' gateways, migrate the VNet and all resources within to ARM

## Recommended Documents

* [Resize a gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-create-gateway-powershell#resize-a-gateway)
* [Platform-supported migration of IaaS resources from classic to Azure Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-overview)