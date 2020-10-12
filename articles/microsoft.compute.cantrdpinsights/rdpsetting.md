<properties
pageTitle="RDP Disabled"
description="RDP Setting"
infoBubbleText="RDP Disabled"
service="microsoft.compute"
resource="virtualmachines"
authors="timbasham"
ms.author="tibasham"
displayOrder=""
articleId="vmhealthsignal_fe8ab797-7bbd-4ec4-9798-7df51f6ca066"
diagnosticScenario="RDP Setting"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# RDP Disabled
<!--issueDescription-->
Remote Desktop has been disabled on the VM <!--$vmname-->[vmname]<!--/$vmname-->.

The REG_DWORD value `fDenyTSConnections` of the registry key `HKLM\System\CurrentControlSet\Control\Terminal Server` is set to 1.
<!--/issueDescription-->

## **Recommended Steps**
**Reset RDP Connection**

Resetting the RDP configuration of the VM can re-establish connectivity in scenarios where Remote Connections are disabled or Windows Firewall rules are blocking RDP.

Steps:

1. [Reset RDP](data-blade:Microsoft_Azure_Compute.VirtualMachinePasswordReset.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/resetPassword)
2. Select `Reset configuration only` and then click `Update`

Please refer to steps on [resetting RDP configuration](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection#troubleshoot-using-the-azure-portal) for more information.
