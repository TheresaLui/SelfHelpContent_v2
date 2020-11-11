<properties
    pageTitle="Azure Virtual Network - Service Chain with Hub-and-Spoke configurations"
    description="Azure Virtual Network - Service Chain with Hub-and-Spoke configurations"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781393"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fe222069-21df-4797-93fe-d4b1cadade96"
/>

# Azure Virtual Network - Service Chain with Hub-and-Spoke configurations

## **Recommended Steps**

Completing a Service Chain in a hub and spoke topology within Azure requires the following steps:

1. Use a Network Virtual Appliance (NVA) in the Hub VNet. [Set up an NVA](https://docs.microsoft.com/azure/virtual-network/tutorial-create-route-table-portal#create-an-nva).

2. There must be [user-defined routes (UDRs)](https://docs.microsoft.com/azure/virtual-network/tutorial-create-route-table-portal#create-a-route-table) in the spoke VNets with the next hop type of **Network Virtual Appliance** pointing to the internet protocol (IP) address of the NVA in the hub virtual network (VNet)

3. NVA network interfaces (NICs) must have ['IP Forwarding' enabled](https://docs.microsoft.com/azure/virtual-network/tutorial-create-route-table-portal#turn-on-ip-forwarding)

4. NVAs must be configured correctly internally, which requires NVA vendor assistance. For point-to-site clients connecting with resources, in a remote VNet that is peered with the point-to-site VPN VNet, ensure the following:

   - The **use remote gateway** option is selected for the spoke VNet that doesn't have a VPN gateway. You won't be able to enable this if your spoke VNet has a gateway by-design.
   - The **allow gateway transit** option must be enabled on the hub VNet that has the point-to-site VPN gateway.
   - The point-to-site package must be downloaded and installed again **after** VNet Peering has been established or changed for the point-to-site package to have the updated routes.

## **Recommended Documents**

- [Service chaining in Azure](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview#service-chaining)
- [Service chaining a hub-and-spoke topology over a site-to-site VPN connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit?toc=%2fazure%2fvirtual-network%2ftoc.json)
- [Service chaining a hub-and-spoke topology over an ExpressRoute connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit?toc=%2fazure%2fvirtual-network%2ftoc.json)
