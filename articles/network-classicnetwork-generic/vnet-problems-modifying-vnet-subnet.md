<properties
    pageTitle="Azure Virtual Network - Problems modifying a VNet or Subnet"
    description="Azure Virtual Network - Problems modifying a VNet or Subnet"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781391"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="52b3038f-c574-4c2f-ba44-9639e9cb8e34"
/>

# Azure Virtual Network - Problems modifying a VNet or Subnet

## **Recommended Steps**

Change a VNet IP range:

1. Add a [new address space](https://docs.microsoft.com/azure/virtual-network/manage-virtual-network#add-or-remove-an-address-range) in the virtual network (VNet) that doesn't overlap with on-premises ranges or VNet ranges that you want to peer with
2. Turn **off** all of the virtual machines (VMs) in the VNet that include the new address space
3. Navigate to each network interface (NIC) and [change the NIC subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface#change-subnet-assignment) from the old subnet to the newly added subnet
4. Remove any other resources from the original address range, such as [private endpoints](https://docs.microsoft.com/azure/private-link/private-endpoint-overview), [subnet delegations](https://docs.microsoft.com/azure/virtual-network/manage-subnet-delegation#remove-subnet-delegation-from-an-azure-service) to other services, and [VNet integrations](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#manage-vnet-integration)
5. After you change the NICs to newly created subnets, [delete the original address space](https://docs.microsoft.com/azure/virtual-network/manage-virtual-network#add-or-remove-an-address-range)

## **Recommended Documents**

- [Add or remove an address range from a VNet](https://docs.microsoft.com/azure/virtual-network/manage-virtual-network#add-or-remove-an-address-range)
- [Add, change, or delete a virtual network subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet)
