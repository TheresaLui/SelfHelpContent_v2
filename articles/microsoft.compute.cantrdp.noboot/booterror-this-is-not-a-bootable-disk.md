<properties
    pageTitle="VM boot error - This is not a bootable disk"
    description="Virtual machine failed to boot with the error this is not a bootable disk"
    infoBubbleText="A boot error 'This is not a bootable disk' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="BootError-THIS_IS_NOT_A_BOOTABLE_DISK"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error 'This is not a bootable disk'
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code **This is not a bootable disk**. If you encounter this error message, it means that the OS boot process could not locate an active system partition. Alternatively, it could mean that there is a missing reference in the Boot Configuration Data (BCD) store, which is preventing it from locating the Windows partition. 
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **This is not a bootable disk. Please insert a bootable floppy and press any key to try again...**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [This is not a Bootable Disk](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-guide-not-bootable-disk) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
