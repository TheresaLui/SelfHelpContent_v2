<properties
pageTitle="CantDeleteVnet"
description="FindVnetAllocations"
infoBubbleText="Issues with Vnet deletion were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="FindVNetAllocations"
diagnosticScenario="FindVnetAllocations"
selfHelpType="diagnostics"
supportTopicIds="32584253"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# We ran diagnostics on your virtual network and found an issue
<!--issueDescription-->
We have identified that the following resource(s) are allocated to the Virtual Network <!--$Vnet-->[Vnet]<!--/$Vnet-->:

<!--$VnetAllocations-->[VnetAllocations]<!--/$VnetAllocations--> 

These resources must be deleted or disassociated with this virtual network prior to deleting.
<!--/issueDescription-->

## **Recommended Steps**

1. Check your [connected devices blade](data-blade:Microsoft_Azure_Network.VirtualNetworkBlade;data-blade-uri:{$domain}) for virtual network. Make sure to delete all the connected devices. If there are any connected devices, deletion of the virtual network will fail.
2. Make sure you have followed all the steps outlined in the [Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet#troubleshooting-guidance) document
3. If you are unable to delete your virtual network due to a resource in failed state within the network, visit **https://resources.azure.com** and navigate to the resource in the failed state. Click on the Edit button followed by the PUT button for the resource in the failed state. This will remove your resource from being in the failed state.

## **Recommended Documents**

* [Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet)
<br>
