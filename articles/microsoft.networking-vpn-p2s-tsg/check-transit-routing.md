<properties
	pageTitle="Check Transit Routing"
	description="Check Transit Routing"
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
	articleId="a31db006-6ea8-48a0-8884-ddfd88494a9a"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check Transit Routing

By default, a Point to Site client will only be able to access the address space of:
* The Virtual Network it is connected to
* Virtual Networks that have a VNet Peering connection to the Virtual Network with the Azure VPN Gateway
* Other local/virtual networks that are connected to the Virtual Network with the Azure VPN Gateway via a site to site connection
* Further local/virtual networks that are connected to the Virtual Network with the Azure VPN Gateway via a sequence of chained connections that use BGP

Connectivity to other networks via a routing hop through the Azure VPN Gateway is called **Transit Routing**.

**Note: By design Point to site clients will NOT have connectivity with remote networks if they are connected via an NVA appliance rather than an Azure VPN Gateway. This is achieved by means of UDRs.** See [Scenario: Route traffic through an NVA](https://docs.microsoft.com/en-us/azure/virtual-wan/scenario-route-through-nva) for more info on this.

Notice also that that transit routing over coexistence gateways is not supported - You cannot route (via Azure) between your local network connected via Site-to-Site VPN and your local network connected via ExpressRoute.

## Recommended Steps
1. Determine VPN Client Protocol
  1. Go to ASC > Resource Explorer and select the VPN gateway.
  2. Check the **VPN Tunneling Protocols** property and identify the protocol.
  3. If more than one protocol has been enabled, ask the customer if the clients failing are using a specific protocol as we cannot tell from the backend.

## Applying solutions

Once VPN protocol is determined you can apply the relevant solution.

**For Windows SSTP clients**, the only requirement is for the client to have a route for the destination network pointing to the VPN gateway. The gateway will take it from there.
* The Point to site client must be injected with a route for each of those destinations.
* You can add such route on the client by means of the **route add** command.
* If you want the route to be added/deleted when the VPN connects/disconnects for Windows clients, you can edit the **%appdata%/Microsoft/Network/Connections/Cm/$gatewayID/routes.txt** file
* Additionally, check if the destination on-prem VPN device has a route for the P2S client IP range

**For OpenVPN clients**, the only requirement is for the client to have a route for the destination network pointing to the VPN gateway. The gateway will take it from there.
* The Point to site client must be injected with a route for each of those destinations.
* OpenVPN clients will leverage the **VpnSettings.xml** file distributed via the Point to site Package so the additional routes must be added there.
* Additionally, check if the destination on-prem VPN device has a route for the P2S client IP range

**IKEv2 clients** need routes to be added to the OS in the **routes.txt** (for Windows) or **VpnSettings.xml** depending on the OS, just like for SSTP/OpenVPN.

However, having a route for the destination network pointing to the VPN gateway is not enough for an IKEv2 client. This is because the Point to Site client and the VPN Gateway establish an IPsec connection that uses narrow traffic selectors. **The Traffic Selectors will only include the routes that the gateway knows about.** So no matter which route you add to the client, it won't work if there isn't a corresponding Traffic Selector sent by the gateway.

You need to review the [IkeLogsTable](https://jarvis-west.dc.ad.msft.net/A5B239BD) at the time of VPN connection establishment to check the Traffic Selector exchanged and verify if the destination the client wants to reach is included in those.
