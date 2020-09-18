<properties
    pageTitle="VM boot error"
    description="Virtual machine failed as it is expecting *user inputs* on the console screen"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ram-kakani,timbasham, jasonbandrew"
    ms.author="ramakk,tibasham, v-jasoan"
    displayOrder=""
    articleId="OSStartUp-INPLACE_UPGRADE"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error
<!--issueDescription-->
We have investigated and determined that your virtual machine **<!--$vmname-->[vmname]<!--/$vmname-->** is in an inaccessible state because Windows is waiting for **user inputs** to complete an ongoing installation/upgrade.
<!--/issueDescription-->

The issue occurs when the OS is performing an in-place upgrade on the VM. You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect that the VM is waiting for setup to be completed.<br>

## **Recommended Steps**

Currently, performing an in-place upgrade on an Azure VM is not supported. However, it can be performed by using a *Nested Hyper-V Environment*:

1. Stop/deallocate the Virtual Machine **<!--$vmname-->[vmname]<!--/$vmname-->** and [save a copy of the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/vhd-copy)
2. Complete the setup using the copy of the OS disk in a [*Nested Hyper-v Environment*](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-vm-by-use-nested-virtualization) and complete the setup process for the *in-place upgrade*
3. Once the disk is fixed, detach the repaired OS disk from the troubleshooting VM that was created in step 2. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap).
