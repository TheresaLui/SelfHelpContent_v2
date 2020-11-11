<properties
    pageTitle="Azure Virtual Network - Issues configuring Azure Virtual Network (VNet) Peering"
    description="Azure Virtual Network - Issues configuring Azure Virtual Network (VNet) Peering"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781389"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c8a04c38-bf37-442b-b9b0-8bba093924c4"
/>

# Azure Virtual Network - Issues configuring Azure Virtual Network (VNet) Peering

## **Recommended Steps**

1. The user setting up this configuration must set **Network Contributor** permissions on both subscriptions

2. [Learn how](https://docs.microsoft.com/azure/virtual-network/create-peering-different-subscriptions) to resolve this issue when both VNets are Azure Resource Managers (ARMs).

3. [Learn how](https://docs.microsoft.com/azure/virtual-network/create-peering-different-deployment-models-subscriptions) to resolve this issue when VNets are in different deployment models

4. If the VNets are in different subscriptions, and the subscriptions are associated with different **Azure Active Directory** tenants, complete the following steps before continuing with the Azure documentation:

   1. Add the user from each Active Directory tenant as a guest user in the opposite Azure Active Directory tenant.

   2. Each user must accept the guest user invitation from the opposite Azure Active Directory tenant.

   3. Run the following PowerShell command:

```
      $vnetA=Get-AzVirtualNetwork -Name "VNET" -ResourceGroupName "RSGRP"
      Add-AzVirtualNetworkPeering -Name "PEERNAME" -VirtualNetwork $vnetA -RemoteVirtualNetworkId
      /subscriptions/SubscriptionID/resourceGroups/Default Networking/providers/Microsoft.ClassicNetwork/virtualNetworks/name
```

## **Recommended Documents**

Step-by-step walk-throughs for creating peerings between:

- [Different subscriptions](https://docs.microsoft.com/azure/virtual-network/create-peering-different-subscriptions)
- [Different deployment models & different subscriptions](https://docs.microsoft.com/azure/virtual-network/create-peering-different-deployment-models-subscriptions)
- [Validate User Permissions in each subscription](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#permissions)
