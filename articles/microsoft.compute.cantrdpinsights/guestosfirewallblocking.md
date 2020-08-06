<properties
pageTitle="Guest OS Firewall blocking all traffic"
description="Guest OS Firewall blocking all traffic"
infoBubbleText="Guest OS firewall is blocking all traffic, impacting RDP connectivity"
service="microsoft.compute"
resource="virtualmachines"
authors="timbasham"
ms.author="tibasham"
displayOrder=""
articleId="GuestOSFirewallBlocking"
diagnosticScenario="Firewall Misconfigured"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
ownershipId="Compute_VirtualMachines_Content"
/>


# Guest OS Firewall is set to block all inbound connections
<!--issueDescription-->
Guest OS firewall on your VM <!--$vmname-->[vmname]<!--/$vmname--> is setup to block all inbound connections including the RDP traffic.
<!--/issueDescription-->

## **Recommended Steps**

Follow the steps in [Azure VM Guest OS firewall is blocking inbound traffic](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/guest-os-firewall-blocking-inbound-traffic) troubleshooting guide to resolve the issue.

