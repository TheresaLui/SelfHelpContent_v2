<properties
	pageTitle="Fix site to Site VPN"
	description="Fix site to Site VPN"
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
	articleId="c64b9fe7-9371-44aa-9a02-ae45fe70a462"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for RADIUS is unreachable because Site to Site VPN is down
From our investigation we've determined that authentication is failing due to the Radius server being unavailable due to the Site-to-Site-VPN connection being down. The gateway must be able to reach the RADIUS server to correctly perform RADIUS authentication for point to Site clients. We recommend the following steps to resolve this issue.

## Recommended Steps

1. Check that the Site to Site VPN is in a connected state as outlined in [this document](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-verify-connection-resource-manager)
2. if RADIUS failure happens because the Site to Site VPN is down, troubleshoot the case using the Site to Site TSG.

## Recommended Documents

* https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-verify-connection-resource-manager
* https://docs.microsoft.com/azure/vpn-gateway/point-to-site-how-to-radius-ps