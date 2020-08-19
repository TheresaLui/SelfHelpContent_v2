<properties
    pageTitle="VM Primary NIC Disabled"
    description="Virtual machine is inaccessible due to the primary NIC being disabled"
    infoBubbleText="Virtual machine is inaccessible due to the primary NIC being disabled"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="PrimaryNICDisabled"
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
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the primary NIC is disabled. This issue occurs if primary NIC is marked as disabled in the Guest OS (Windows).
<!--/issueDescription-->

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows Network Interface is disabled](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nic-disabled) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP in Azure VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
