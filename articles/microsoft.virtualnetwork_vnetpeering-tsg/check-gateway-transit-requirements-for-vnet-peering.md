<properties
	pageTitle="TSG Content Step: check gateway transit requirements for vnet peering"
	description="TSG Content Step: check gateway transit requirements for vnet peering"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3fa05c06-d04a-4c80-a397-f43e5d228a00"
/>

# Check gateway transit requirements for vnet peering

For resources in a spoke VNET to communication with on-premises resources in a hub and spoke topology, gateway transit settings must be configured on spoke VNet and the Hub VNet.

1. *'Use Remote Gateway'* must be enabled on the spoke VNet (that does not have the gateway)
2. *'Allow Gateway Transit'* must be enabled on the hub VNet (that has the gateway)
3. *'Allow Forwarded Traffic'* must be enabled on the hub VNet (that has the gateway)
4. Limitation: Cannot use VNet alone to transit between spokes (on-prem or in Azure)

   * See [Service Chaining](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview#service-chaining) OR
   * See [VPN/ExR Coexistence gateways](https://docs.microsoft.com/azure/expressroute/expressroute-howto-coexist-resource-manager#configure-a-site-to-site-vpn-to-connect-to-sites-not-connected-through-expressroute) for on-premises spokes

## **Recommended Steps**

1. Use *'Network Topology'* in ASC > Tools

   1. Browse to *'Network Topology'* in ASC > Tools
   2. Login and select the button 'Generate New Topology' if needed
   3. Click on the arrows connecting the VNets and click 'Show more' in the right hand properties pane

      1. Select the line where the spoke VNet is the 'Source' VNet in the properties pane
      2. Check the 'Use Remote Gateway' field. It should be set to 'True' (If it is not have the customer fix.
      3. Select the line where the hub VNet (with the gateway) is the 'Source' VNet in the properties pane
      4. Check the 'Allow Gateway Transit' field. It should be set to 'True' (If it is not have the customer fix.
2. Alternatively, use *'Resource Explorer'* in ASC

   1. Find the spoke VNet that does not have the gateway
   2. Select Properties > Peerings and expand the peering
   3. Check the 'Use Remote Gateway' field. It should be set to 'True' (If it is not have the customer fix.
   4. Fine the hub VNet that has the gateway in it
   5. Select Properties > Peerings and expand the peering
   6. Check the 'Allow Gateway Transit' field. It should be set to 'True' (If it is not have the customer fix.

## **Recommended Documents**

1. [Configure VPN Gateway transit for virtual network peering](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit?toc=%2fazure%2fvirtual-network%2ftoc.json)


