<properties
    pageTitle="Azure Virtual Network - VNet Peering with on-premises resources"
    description="Azure Virtual Network - VNet Peering with on-premises resources"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781399"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2187bd76-bd45-43bf-ad90-5aa286f9e04f"
/>

# Azure Virtual Network - VNet Peering with on-premises resources

## **Recommended Steps**

For point-to-site clients connecting with resources in a remote virtual network (VNet), that is peered with the point-to-site virtual private network (VPN) VNet, ensure the following:

   1. The **use remote gateway** option is selected for the spoke VNet that doesn't have a VPN gateway. (You won't be able to enable this if your spoke VNet has a gateway by-design)
   2. The **allow gateway transit** option must be enabled on the hub VNet that has the point-to-site VPN gateway.
   3. The point-to-site package must be downloaded and installed again **after** VNet Peering has been established or changed for the point-to-site package to have the updated routes.

## **Recommended Documents**

- [Service chaining a hub-and-spoke topology over a site-to-site VPN connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit?toc=%2fazure%2fvirtual-network%2ftoc.json)
- [Service chaining a hub-and-spoke topology over an ExpressRoute connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit?toc=%2fazure%2fvirtual-network%2ftoc.json)
