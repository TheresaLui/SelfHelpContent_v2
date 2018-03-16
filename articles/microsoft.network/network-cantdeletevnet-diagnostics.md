<properties
pageTitle="CantDeleteVnet"
description="FindVnetAllocations"
infoBubbleText="FindVnetAllocations"
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="FindVnetAllocations"
diagnosticScenario="FindVnetAllocations"
selfHelpType="diagnostics"
supportTopicIds="32584253"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="public"
/>
# Vnet Allocation Diagnostic Result
<!--issueDescription-->
## Problems Identified
Microsoft Azure has identified Vnet <!--$Vnet-->[Vnet]<!--/$Vnet--> as having the following resource/s allocated: <!--$VnetAllocations-->[VnetAllocations]<!--/$VnetAllocations-->. These resources must be deleted or disassociated with Vnet <!--$Vnet-->[Vnet]<!--/$Vnet--> prior to deleting. 
 ## **Recommended steps**
To resolve the most common issues, try one or more of the following methods.
1. Check your [Connected devices](data-blade:Microsoft_Azure_Network.ConnectionInfoBlade) blade of the virtual network. Make sure to delete all the connected devices. If there are any connected devices, deletion of the virtual network will fail.
2. Make sure you have followed all the steps outlined in the [Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet#troubleshooting-guidance) document.
3. If you are unable to delete your virtual network due to a resource in failed state within the network visit [resources.azure.com](https://resources.azure.com/) and navigate to the resource in the failed state. Then click on the Edit button followed by the PUT button for the resource in the failed state. This will remove your resource from being in the failed state.<br>
## **Recommended documents**
[Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet)
<br>
<!--/issueDescription-->
