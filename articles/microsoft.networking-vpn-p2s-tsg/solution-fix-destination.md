<properties
	pageTitle="Fix Destination"
	description="Fix Destination"
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
	articleId="feafd94f-5e0e-487c-96c7-2976b9fd1d36"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for fixing the point to site client

We found through troubleshooting that the point-to-site client causes this issue not sending the traffic down the VPN tunnel. The following can cause this:

- Incorrect routes (SSTP or OpenVPN)
- Incorrect Traffic Selectors (IKEv2)
- Misbehaving Third party software


## Recommended Steps 
(Needs validation) <br>
**For SSTP clients** the only requirement is for the client to have a route for the destination network pointing to the VPN gateway.

1. You can add such route on the client by means of the **route add** command.
   * If you want the route to be added/deleted when the VPN connects/disconnects for Windows clients, you can edit the **%appdata%/Microsoft/Network/Connections/Cm/$gatewayID/routes.txt** file
2. Additionally, check if the destination on-prem VPN device has a route for the P2S client IP range

**For OpenVPN clients**, the only requirement is also for the client to have a route for the destination network pointing to the VPN gateway.

1. OpenVPN clients will leverage the **VpnSettings.xml** file distributed via the Point to site Package so the additional routes must be added there.
2. Additionally, check if the destination on-prem VPN device has a route for the P2S client IP range

**For IKEv2 clients**

1. IKEv2 clients need routes to be added to the OS in the **routes.txt** (for Windows) or **VpnSettings.xml** depending on the OS, just like for SSTP/OpenVPN.
2. However, having a route for the destination network pointing to the VPN gateway is not enough for an IKEv2 client. This is because the Point to Site client and the VPN Gateway establish an IPsec connection that uses narrow traffic selectors. **The Traffic Selectors will only include the routes that the gateway knows about.** So no matter which route you add to the client, it won't work if there isn't a corresponding Traffic Selector sent by the gateway.
3. Engage the Client OS vendor. If this is a Windows client, engage Windows onprem networking team.**
