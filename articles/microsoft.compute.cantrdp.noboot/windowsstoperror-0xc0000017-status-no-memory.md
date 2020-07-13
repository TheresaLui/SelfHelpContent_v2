<properties
    pageTitle="VM boot error: 0xC0000017 Status No Memory"
    description="Virtual machine failed to boot with error code 0xC0000017, which means 'Status No Memory'. You may see this error listed in either Windows Boot Manager, or the Recovery screen, depending upon the Windows version you are running."
    infoBubbleText="Windows failed to start with the error code 0xC0000017, which means 'Status No Memory'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0xC0000017-STATUS_NO_MEMORY"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: #0xC0000017 Status No Memory
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because there's not enough virtual memory or paging file quota available to complete the specified operation. This can be due to a full or fragmented operating system disk, or because the operating system is unable to read access memory and/or the pagefile.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **0xC0000017**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows stop error: 0xC0000017 Status No Memory](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-windows-stop-error) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
