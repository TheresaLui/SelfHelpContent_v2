<properties
pageTitle="RDPListener misconfigured"
description="RDP-TCP listener misconfigured"
infoBubbleText="RDP-TCP listener misconfigured"
service="microsoft.compute"
resource="virtualmachines"
authors="timbasham"
ms.author="tibasham"
displayOrder=""
articleId="vmhealthsignal_451e7e7e-0aae-4145-ae1b-e761548a36d7"
diagnosticScenario="RDP listener"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>


# RDP-TCP listener is misconfigured
<!--issueDescription-->

## Recommended Steps**

We have investigated and identified that the RDP-TCP listener is misconfigured, which impacts RDP connectivity to this virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. To regain RDP connectivity, reconfigure the listener through the serial console or other remote management options, as described in the following documentation.
<!--/issueDescription-->

## **Recommended Documents**

See [Troubleshoot authentication errors when you use RDP to connect to Azure VM](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/cannot-connect-rdp-azure-vm)
