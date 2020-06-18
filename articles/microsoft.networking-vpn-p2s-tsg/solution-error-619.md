<properties
	pageTitle="Solution for VPN Point-to-Site client error 619"
	description="Solution for VPN Point-to-Site client error 619"
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
	articleId="761ac71e-9225-439a-a1a6-4289286026b5"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 619

The error *"Error 619: a connection to the remote computer could not be established"* implies failures in the RADIUS server connectivity. The behavior typically resembles this: when attempting to establish connectivity the client hangs for about 60 seconds and then displays error message 619. This means the RADIUS server is reachable from the gateway, but the RADIUS conversation between gateway and RADIUS server fails because of RADIUS specific issues on the server.


## Recommended Steps

1. Have a server administrator review the performance and reliability of the RADIUS server 
2. If the RADIUS server is on-premises, check the status of the site to site VPN connection as outlined in [this document](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-verify-connection-resource-manager)


## Recommended Documents

* [Microsoft Server Performance Advisor](https://docs.microsoft.com/windows-server/networking/technologies/network-subsystem/net-sub-performance-tools#bkmk_advisor)
* [Verify a VPN Gateway connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-verify-connection-resource-manager)
* [Troubleshooting: Azure Site-to-Site VPN disconnects intermittently](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently)
