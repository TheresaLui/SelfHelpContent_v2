<properties
	pageTitle="SSTP does not support this scenario"
	description="Mac OS version does not support this scenario"
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
	articleId="2f8b3ac9-2697-4c99-a646-a24db8407a8d"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for SSTP does not support this scenario

We found that this is not a supported scenario. SSTP is limited to maximum 128 clients. This is a hard-coded limit across all gateway SKUs and cannot be increased.

## Recommended Steps

1. Connect less than 127 clients to each gateway
2. Use a different protocol such as IKEv2 or OpenVPN
3. Use a 3rd party Network Virtual Appliance (NVA) solution

## Recommended Documents

* [Which gateway SKUs support P2S VPN?](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#gwsku)
* [What protocol does P2S use?](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#protocol)
* [Azure Marketplace Network Virtual Appliances](https://azure.microsoft.com/solutions/network-appliances/)