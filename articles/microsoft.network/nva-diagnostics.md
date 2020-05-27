<properties
pageTitle="NvaDiagnostic"
description="NvaDiagnostic"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="NvaDiagnosticsInsight"
diagnosticScenario="NvaDiagnosticsInsight"
selfHelpType="Diagnostics"
supportTopicIds="32584252, 32584251, 32584250, 32584249, 32547215"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We found an issue related to a Network Virtual Appliance used in this connectivity path
<!--issueDescription-->  
We have assessed the routing from the source VM **'<!--$SourceVM-->[SourceVM]<!--/$SourceVM-->'** and found there is a Network Virtual Appliance (NVA) named **'<!--$NvaVmName-->[NvaVmName]<!--/$NvaVmName-->'** managing the traffic. We ran some diagnostics on the detected scenario and found the following:

- Checked source VM health: **<!--$SourceVmHealthStatus-->[SourceVmHealthStatus]<!--/$SourceVmHealthStatus-->**
- Checked NVA VM health: **<!--$NvaHealthStatus-->[NvaHealthStatus]<!--/$NvaHealthStatus-->**
- Checked destination VM health (if applicable): **<!--$DestVmHealthStatus-->[DestVmHealthStatus]<!--/$DestVmHealthStatus-->**
- Checked the status of 'IP Forwarding' on the NVA NIC: **<!--$IpFwdStatus-->[IpFwdStatus]<!--/$IpFwdStatus-->**
- Checked for Network Security Groups (NSGs) blocking traffic from source VM to NVA VM: **<!--$SourceToNvaNsgStatus-->[SourceToNvaNsgStatus]<!--/$SourceToNvaNsgStatus-->** <br><br>
<!--/issueDescription-->

See below for detailed steps on resolving detected issues.

## **Recommended Steps**

- **Fix Source, NVA, or Destination VM Health Issues:** Check to make sure the VM is in a running state. If it is in a running state, choose the 'Redeploy' button in the portal.
- **Enable IP Forwarding on NVA NIC:** A Network Virtual Appliance (NVA) must have IP forwarding enabled on its Network Interface Card (NIC). To enable IP forwarding on the NVA NIC:

   1. Find the NIC in the portal and  
   2. Select the 'IP configurations' blade <br>
   3. Select the 'Enabled' option for the 'IP Forwarding' field

- **Fix Network Security Groups:** If the access control (security rules) result is not desired, view the Effective Security Rules to determine if the addition or modification of a customer-defined security rule is required:

   1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
   2. Click Browse > Network Interface
   3. Select the Network Interface of your VM
   4. Click on the Effective routes blade
   5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network

## **Recommended Documents**

* [Redeploy troubleshooting](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows#use-the-azure-portal)
* [Enabling IP forwarding](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface#enable-or-disable-ip-forwarding)
* [How to troubleshoot NVA devices](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)
