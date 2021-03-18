<properties
    pageTitle="Azure Virtual Network - Cannot delete VNet because of other resources"
    description="Azure Virtual Network - Cannot delete VNet because of other resources"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781381"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ad126fcf-7e81-4bed-b6c3-0c7901ea946d"
/>

# Azure Virtual Network - Cannot delete VNet because of other resources

Clean up the resources within this virtual network before deleting.

## **Recommended Steps**

1. Check your [connected devices blade](https://ms.portal.azure.com/) for your virtual network. Delete all the connected devices. If there are any connected devices, you can't delete the virtual network.

2. Follow **all** steps outlined in the [Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet?WT.mc_id=Portal-Microsoft_Azure_Support#troubleshooting-guidance) document.

3. If you're unable to delete your virtual network due to a resource in failed state within the network, visit [https://resources.azure.com](https://resources.azure.com) and navigate to the resource in the failed state. Select the **Edit** button, then the **PUT** button, for the resource in the failed state. This will address your resource being in the failed state.

## **Recommended Documents**

Delete the most common resources which may cause issues when deleting your virtual network:

- [VPN Gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-delete-vnet-gateway-portal)
- [Application Gateway](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet#check-whether-an-application-gateway-is-running-in-the-virtual-network)
- [Express Route connection](https://docs.microsoft.com/azure/expressroute/expressroute-howto-linkvnet-portal-resource-manager#delete-a-connection-to-unlink-a-vnet)
- [Virtual Network peering](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#delete-a-peering)
- [Subnet Delegation](https://docs.microsoft.com/azure/virtual-network/manage-subnet-delegation#remove-subnet-delegation-from-an-azure-service-1)
