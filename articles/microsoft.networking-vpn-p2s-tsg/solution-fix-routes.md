<properties
	pageTitle="Fix the routes"
	description="Fix the routes"
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
	articleId="16e0f41d-3045-449d-8b36-1042ab77e323"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for missing routes on the point-to-site client 

We found that there are missing routes on the point-to-site client. Please follow the steps below to resolve


## Recommended Steps

1. Add missing routes to the client
   1. Use the route add command
   2. To add/delete route when the VPN connects/disconnects for Windows clients, you can edit the 
 appdata%/Microsoft/Network/Connections/Cm/$gatewayID/routes.txt file
   3. MAC OS and OpenVPN clients instead will leverage the VpnSettings.xml file distributed via the Point to site Package so the additional routes must be added there.
2. Make sure all local network objects linked to the VPN gateway are correctly configured according to on-premises network subnet allocations


# Recommended Documents

* [Route commands](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/ff961510(v=ws.11))
* [Configure on-premises network subnet allocations](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal#LocalNetworkGateway)