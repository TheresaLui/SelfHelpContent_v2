<properties
    pageTitle="VM boot error: #0xC0000225 'Status not found'"
    description="Virtual machine failed to boot due to error code #0xC0000225 with the message 'Status not found'"
    infoBubbleText="A Windows Boot Manager prompt 'Windows failed to start' or the Recovery screen with message 'Your PC/Device needs to be repaired' with the Status/Error code: #0xC0000225"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsBootManager-0xC0000225-STATUS_NOT_FOUND"
    diagnosticScenario="windowsbootmanager"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: #0xC0000225 'Status not found'
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because either: A) There is missing or corrupted binary on your System file. B) There's Boot Configuration Data (BCD) corruption or an improperly prepared VHD that was migrated from on-premise, that resulted in the ommission of the OSDEVICE variable. C) A registry error such as hive failure, a mounted but empty hive, or an improper closure of a hive.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **0xC0000225**, also known as **Status not found**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows Boot Manager error: 0xC0000225 "Status not found"](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-status-not-found) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
