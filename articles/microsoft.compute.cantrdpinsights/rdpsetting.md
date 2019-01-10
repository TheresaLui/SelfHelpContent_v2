<properties
pageTitle="RDP Disabled"
description="RDP Setting"
infoBubbleText="RDP Disabled"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_fe8ab797-7bbd-4ec4-9798-7df51f6ca066"
diagnosticScenario="RDP Setting"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# RDP Disabled
<!--issueDescription-->
The Remote Desktop has been set to disabled on the VM.

The REG_DWORD value `fDenyTSConnections` of the registry key  `HKLM\System\CurrentControlSet\Control\Terminal Server` is set to 1.
<!--/issueDescription-->

## **Recommended Steps**
**Reset RDP Connection**

Resetting RDP configuration will establish connectivity in scenarios where Remote Connections are disabled or Windows Firewall rules are blocking RDP.

Steps:

1. Select your VM in the Azure portal
2. Scroll down the settings pane to the Support + Troubleshooting section near bottom of the list
3. Click the Reset password button. Set the Mode to Reset configuration only and then click the Update button

  Please refer to steps on [resetting RDP configuration](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection#troubleshoot-using-the-azure-portal) in the public article.
