<properties
    pageTitle="No Active NIC Found"
    description="No active NICs were found in Guest OS of the VM"
    infoBubbleText="No active NICs were found in Guest OS of the VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="NoActiveNic"
    diagnosticScenario="No active NIC found"
    selfHelpType="diagnostics"
    supportTopicIds="32615525"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# No active network interface cards (NIC) were found in the VM guest OS
<!--issueDescription-->
We have investigated and detected that the virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> does not currently appear to have any active NICs.
<!--/issueDescription-->

## **Recommended Steps**

* [Activating or resetting the guest NIC](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nic-disabled) may restore RDP connectivity to the VM <!--$vmname-->[vmname]<!--/$vmname-->
