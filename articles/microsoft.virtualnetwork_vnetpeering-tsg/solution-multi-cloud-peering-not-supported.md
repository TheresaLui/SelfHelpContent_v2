<properties
	pageTitle="Multi cloud peering not supported"
	description="Multi cloud peering not supported"
	service="microsoft.network"
	resource="virtualNetwork"
	authors="chadmath"
	ms.author="chadmat"
	diagnosticScenario="MultiCloudPeeringNotSupported"
	selfHelpType="TSG_Content"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	articleId="7248de1e-cf9b-4bbd-9ee5-b0f32fd0a4f6"
	ownershipId="Centennial_Cloudnet_VirtualNetwork"
	supportTopicIds=""
    resourceTags="windows"
    productPesIds="15526"
/>

# VNet Peering across cloud types not supported
<!--issueDescription-->

Through our investigation we found that peering Virtual Networks across different Azure cloud types such as 'Public' and 'Government' is not supported. Please refer to the article below for more information on the limitation and options on connecting VNets across Azure clouds.

<!--/issueDescription-->


## **Recommended Documents**

* [Vnet Peering Constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#requirements-and-constraints)
* [Configure a VNet-to-VNet VPN gateway connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager-portal)