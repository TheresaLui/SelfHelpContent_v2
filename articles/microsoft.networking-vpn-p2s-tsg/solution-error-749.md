<properties
	pageTitle="Solution for VPN Point-to-Site client error 749"
	description="Solution for VPN Point-to-Site client error 749"
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
	articleId="c37737d7-e37b-4cbd-8c1f-ae5b9e56dfca"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 749

The error *"Error 749: The destination address or phone number is either invalid or not present"* means that the VPNprofile.XML for the Device Tunnel is not configured properly.

## Recommended Steps

1. Verify that the FQDN of the gateway is correctly reported in the <Server> section of the VPNprofile.XML.
2. Verify that the <Routes> section of the VPNprofile.XML correctly contains the vnet address space.

## Recommended Documents

* https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-always-on-device-tunnel
