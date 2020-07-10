<properties
    pageTitle="VM DHCP Disabled"
    description="Virtual machine is inaccessible due to DHCP client service being disabled"
    infoBubbleText="Virtual machine is inaccessible due to DHCP client service being disabled"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="WindowsGuestDhcpDisabled"
    diagnosticScenario="cannotconnectrdp"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Cannot connect to VM using RDP
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the DHCP client service is disabled. This issue occurs if the DHCP client service is disabled on the NIC in the Guest OS (Windows).
<!--/issueDescription-->

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [DHCP Client service is disabled](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-dhcp-disabled) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP in Azure VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
