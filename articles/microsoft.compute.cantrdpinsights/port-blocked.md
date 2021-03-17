<properties
pageTitle="Cannot connect to Virtual Machine because of blocked port"
description="Cannot connect to Virtual Machine because of blocked port"
infoBubbleText="Port scan result for your VM. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="clandis"
ms.author="clandis"
displayOrder=""
articleId="port-blocked"
diagnosticScenario="PortBlocked"
selfHelpType="Diagnostics"
supportTopicIds="32411835"
resourceTags="windows,linux"
productPesIds="14749,15571,15797,16454,16470"
cloudEnvironments="public,fairfax,usnat,ussec"
ownershipId="Compute_VirtualMachines_Content"
/>

# RDP or SSH Port Did Not Respond to Port Scan

<!--issueDescription-->
Virtual machine **'<!--$VMArray-->VMArray<!--/$VMArray-->'** did not respond to a port scan of port  **'<!--$PortsArray-->PortsArray<!--/$PortsArray-->'**.
<!--/issueDescription-->

## **Recommended Steps**

### Windows

1. Verify [RDP is enabled](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/reset-rdp#reset-the-remote-desktop-services-configuration).

2. Verify the [Windows guest firewall allows port TCP 3389 inbound](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/guest-os-firewall-blocking-inbound-traffic).

3. Verify the [Azure network security group allows TCP port 3389 inbound](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/troubleshoot-rdp-nsg-problem).

### Linux

1. Verify SSH is enabled by [resetting the SSH configuration](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/troubleshoot-ssh-connection#reset-the-ssh-configuration).

2. Verify the Linux guest firewall allows TCP port 22 inbound.

3. Verify the [Azure network security group allows port TCP 22 inbound](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/detailed-troubleshoot-ssh-connection#source-4-network-security-groups).
