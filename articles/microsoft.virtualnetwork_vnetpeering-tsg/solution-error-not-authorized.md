<properties
pageTitle="Solution for error 'TENANT ID' is not authorized to access linked subscription 'SUBID'"
description="Solution for error 'TENANT ID' is not authorized to access linked subscription 'SUBID'"
infoBubbleText="Solution for error 'TENANT ID' is not authorized to access linked subscription 'SUBID'"
service="microsoft.network"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionForErrorTenantNotAuthorized"
diagnosticScenario="SolutionForErrorTenantNotAuthorized"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
/>
# Solution for cross subscription virtual network peering
<!--issueDescription-->

The user setting up peering across subscriptions must have **'Network Contributor'** permissions on both subscriptions. There are also some additional considerations outlined below.

<!--/issueDescription-->


## **Recommended Steps**

1. Please visit this [link](https://docs.microsoft.com/azure/virtual-network/create-peering-different-subscriptions) to resolve this issue when **both VNets are ARM**
2. Please visit this [link](https://docs.microsoft.com/azure/virtual-network/create-peering-different-deployment-models-subscriptions) to resolve this issue when **Vnets are in different deployment models**
3. If the virtual networks are in different subscriptions, and the subscriptions are associated with different Azure Active Directory tenants, complete the following steps before continuing with the Docs documentation:
      1. Add the user from each Active Directory tenant as a guest user in the opposite Azure Active Directory tenant.
      2. Each user must accept the guest user invitation from the opposite Azure Active Directory tenant.
      3. Then run the following PowerShell command: 
      
If the remote VNET is Classic model, use the below command:
~~~PowerShell
$vnetA=Get-AzVirtualNetwork -Name "VNET" -ResourceGroupName "RSGRP"
Add-AzVirtualNetworkPeering -Name "PEERNAME" -VirtualNetwork $vnetA -RemoteVirtualNetworkId
/subscriptions/SubscriptionID/resourceGroups/Default Networking/providers/Microsoft.ClassicNetwork/virtualNetworks/name
~~~
If the remote VNET is ARM model, use the below command:
~~~PowerShell
$vNetA=Get-AzVirtualNetwork -Name myVnetA -ResourceGroupName myResourceGroupA
Add-AzVirtualNetworkPeering `
  -Name 'myVnetAToMyVnetB' `
  -VirtualNetwork $vNetA `
  -RemoteVirtualNetworkId "/subscriptions/<SubscriptionB-Id>/resourceGroups/myResourceGroupB/providers/Microsoft.Network/virtualNetworks/myVnetB"
~~~

## **Recommended Documents**

* [Create Peering from different subscriptions](https://docs.microsoft.com/azure/virtual-network/create-peering-different-subscriptions)
* [Create Peering from different deployment models and in different subscriptions](https://docs.microsoft.com/azure/virtual-network/create-peering-different-deployment-models-subscriptions)
* [Manage permissions for Peering setup](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#permissions)
