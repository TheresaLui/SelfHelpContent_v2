<properties
	pageTitle="check-active-active-both-connected"
	description="check-active-active-both-connected"
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
	articleId="9b3509a8-733a-43d0-b6d2-dece70347562"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if both Active Active gateways of the site to site tunnel are connected

When only one of the VPN gateways is connected in an Active Active configuration, point to site clients may fail to reach destination.

## Recommended Steps

1. In the Azure portal, click 'All Resources' and navigate to your **Virtual Network Gateway**.
2. On the blade for your virtual network gateway, click **Connections**. You can see the status of each connection.

***Notice***: By design the Azure Vpn Gateway will try to connect both connections. If only one is established, it may mean that the on-premises device is misconfigured/refusing the connection.

## Recommended Documents

1. [Verify a VPN Gateway connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-verify-connection-resource-manager)
