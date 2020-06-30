<properties
    pageTitle="VM boot error: Disk read error occurred"
    description="Virtual machine failed to boot due to corrupted disk structure that prevents the disk from being read in your Azure virtual machine."
    infoBubbleText="The VM is stuck in a reboot loop with the message: 'A disk read error occurred. Press Ctrl+Alt+Del to restart'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="BootError-DISK_READ_ERROR_OCCURRED"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Disk read error occurred
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the disk structure is corrupted and unreadable. If you are using a Generation 1 VM, it's also possible that the disk partition containing the boot configuration data isn’t set to Active.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **A disk read error occurred. Press Ctrl+Alt+Del to restart**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Boot error: Disk read error occurred](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-disk-read-error-occurred) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
