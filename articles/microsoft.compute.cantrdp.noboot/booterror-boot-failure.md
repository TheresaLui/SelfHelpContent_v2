<properties
    pageTitle="VM boot error - Boot failure - Insert boot media in selected boot device"
    description="Virtual machine failed to boot with the error Boot failure - Insert boot media in selected boot device"
    infoBubbleText="A boot error 'Boot failure - Insert boot media in selected boot device' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="BootError-BOOT_FAILURE"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error - Boot failure - Insert boot media in selected boot device'
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code **Boot failure. Reboot and Select proper Boot device or Insert Boot Media in selected Boot device**. If you encounter this error message, it means that the OS boot process could not locate an active system partition. Alternatively, it could mean that there is a missing reference in the Boot Configuration Data (BCD) store, which is preventing it from locating the Windows partition. 
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Boot failure. Reboot and Select proper Boot device or Insert Boot Media in selected Boot device**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Troubleshoot Windows VM OS boot failure](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/os-bucket-boot-failure) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
