<properties
	pageTitle="TSG Content Step: Check if re-installing the p2s client package resolves"
	description="TSG Content Step: Check if re-installing the p2s client package resolves"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="15a0f971-e414-4585-9fe9-48261f0a279d"
/>

# Check if re-installing the p2s client package resolves

Point-to-Site client downloads only have the network configuration at the time of the download. Updates to the VNet routing/topology, such as newly peered Vnet routes, are not automatically added to P2S clients so the point-to-site client packages must be redownloaded or the routes must be added manually.

## **Recommended Steps**

1. Download P2S client package on the P2S client
2. Install P2S client package
3. Test connectivity

## **Recommended Documents**

* [routes must be added manually](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/134255/Point-to-Site-VPN-Issues?anchor=transit-routing#transit-routing)


