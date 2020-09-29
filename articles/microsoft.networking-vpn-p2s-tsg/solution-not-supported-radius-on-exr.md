<properties
	pageTitle="Not Supported - RADIUS on ExR"
	description="Not Supported - RADIUS on ExR"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="f219a9b7-0a9d-46fb-8c05-6b53e1614e30"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for RADIUS connected via Expressroute not supported

We found that this is not a supported scenario. The Azure public documentation states "_Only a VPN Site-to-Site connection can be used for connecting to a RADIUS server on-premises. An ExpressRoute connection cannot be used._"

## Recommended Steps

1. Use a site-to-site VPN connection to connect your VNet to your on-premises RADIUS server or
2. Move your RADIUS server into your VNet

## Recommended Documents

* [Configure a Point-to-Site connection to a VNet using RADIUS authentication](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-how-to-radius-ps)

