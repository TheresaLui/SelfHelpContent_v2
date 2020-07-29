<properties
	pageTitle="solution-check-active-active-both-connected"
	description="solution-check-active-active-both-connected"
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
	articleId="81610b57-dcd6-4ee8-be37-272f282d0a49"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Active Active gateways not having all connections up

We found the cause of some point-to-site clients not connecting to resources was due to one of the Active Active VPN gateways not connected. When only one of the VPN gateways is connected in an Active Active configuration, point to site clients may fail to reach destination. When Active Active is enabled for VPN gateways, the Point to site range is divided between the two gateway instances.

## Recommended Steps

1. In the Azure portal, click 'All Resources' and navigate to your **Virtual Network Gateway**.
2. On the blade for your virtual network gateway, click **Connections**. You can see the status of each connection.
3. For any connections in a not connected state, enable the connection

***Notice***: By design the Azure Vpn Gateway will try to connect both connections. If only one is established, it may mean that the on-premises device is misconfigured/refusing the connection.

## Recommended Documents

1. [Verify a VPN Gateway connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-verify-connection-resource-manager)
2. [Troubleshoot VPN disconnects](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently)
