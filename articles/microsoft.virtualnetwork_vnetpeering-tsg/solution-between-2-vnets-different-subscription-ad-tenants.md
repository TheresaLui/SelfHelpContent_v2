<properties
pageTitle="SolutionBetween2VnetsDifferentSubscriptionAdTenants"
description="SolutionBetween2VnetsDifferentSubscriptionAdTenants"
infoBubbleText="SolutionBetween2VnetsDifferentSubscriptionAdTenants"
service="microsoft.network"
ownershipid="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionBetween2VnetsDifferentSubscriptionAdTenants"
diagnosticScenario="SolutionBetween2VnetsDifferentSubscriptionAdTenants"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, fairfax, usnat, ussec"
/>
# Solution for cross subscription virtual network peering
<!--issueDescription-->

From our interaction, it appears that you are looking for steps on how to setup VNet peering between VNets that are in different subscriptions or Active Directory Tenants

<!--/issueDescription-->


## **Recommended Steps**

1. The user setting this up must have **'Network Contributor'** permissions on both subscriptions
2. Please visit this [resource](https://docs.microsoft.com/azure/virtual-network/create-peering-different-subscriptions) to resolve this issue when **both VNets are ARM**
3. Please visit this [resource](https://docs.microsoft.com/azure/virtual-network/create-peering-different-deployment-models-subscriptions) to resolve this issue when **Vnets are in different deployment models**
4. If the virtual networks are in different subscriptions, and the subscriptions are associated with different Azure Active Directory tenants, complete the following steps before continuing with the Azure documentation:
      1. Add the user from each Active Directory tenant as a guest user in the opposite Azure Active Directory tenant.
      2. Each user must accept the guest user invitation from the opposite Azure Active Directory tenant.
      3. Then run the following PowerShell command: 

~~~PowerShell
$vnetA=Get-AzVirtualNetwork -Name "VNET" -ResourceGroupName "RSGRP"
Add-AzVirtualNetworkPeering -Name "PEERNAME" -VirtualNetwork $vnetA -RemoteVirtualNetworkId
/subscriptions/SubscriptionID/resourceGroups/Default Networking/providers/Microsoft.ClassicNetwork/virtualNetworks/name
~~~

## **Recommended Documents**

* https://docs.microsoft.com/azure/virtual-network/create-peering-different-subscriptions
* https://docs.microsoft.com/azure/virtual-network/create-peering-different-deployment-models-subscriptions
* https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#permissions
