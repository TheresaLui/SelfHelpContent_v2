<properties
	pageTitle="Solution for VPN Point-to-Site client error 1292"
	description="Solution for VPN Point-to-Site client error 1292"
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
	articleId="af4484d8-aa9d-45ce-a1df-3431d939d553"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 1292

This issue happens when *all* of the IP addresses in the Point to Site client range have been allocated to connected clients and one or more clients try to connect. The client will get error *"Error 1292: An operation attempted to exceed an implementation-defined limit"*

## Recommended Steps

1. Increase the size of the Point to Site client range to a bigger subnet.

## Recommended Documents

* [Add the VPN client address pool](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-rm-ps#addresspool)
