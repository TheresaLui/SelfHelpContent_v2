<properties
	pageTitle="Known routing issue affecting SSTP VPNs"
	description="Known routing issue affecting SSTP VPNs"
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
	articleId="ea93cec7-16c2-4bb9-a745-ad90fcf1e855"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check for known routing issue affecting SSTP VPNs

There is a known Routing and Remote Access issue for which point to site SSTP clients can connect successfully, but RRAS fails to assign them a route for the virtual network. Hence the client cannot reach anything in the Vnet. This is a Windows OS bug out of the Azure VPN team control. Sadly, the logs don't show the issue. (it took years to debug for that) You can just see if you think that you are using SSTP and don't reach anything.

## Recommended Steps

1. Gateway Resets mitigates the issue (2 Resets might be required).
1. As a long-term solution, it is advised to use IKEv2 rather than SSTP
1. For P2S clients trying to reach Storage accounts follow this [TSG](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/285097/Azure-P2S-connecting-to-Storage)

## **Recommended Documents**

1. [Windows OS Work item for SSTP bug](https://microsoft.visualstudio.com/OS/_workitems/edit/21097365)
