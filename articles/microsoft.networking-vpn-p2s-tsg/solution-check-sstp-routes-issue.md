<properties
	pageTitle="Solution for known routing issue affecting SSTP VPNs"
	description="Solution for known routing issue affecting SSTP VPNs"
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
	articleId="c957998b-bc5c-4af8-bc46-7655d73516ba"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for known routing issue affecting SSTP VPNs

We found that this issue is a known Routing and Remote Access issue for which point to site SSTP clients can connect successfully, but RRAS fails to assign them a route for the virtual network. Hence the client cannot reach anything in the Vnet. This issue is currently being tracked by the Windows product group. The steps below mitigate the issue.

## Recommended Steps

1. Gateway Resets mitigates the issue (2 Resets might be required).
1. As a long-term solution, it is advised to use IKEv2 rather than SSTP

## **Recommended Documents**

1. [Reset VPN Gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic)
2. [Point-to-site IKEv2](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#does-azure-support-ikev2-vpn-with-windows)
