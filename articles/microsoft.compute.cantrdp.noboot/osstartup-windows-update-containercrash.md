<properties
    pageTitle="VM boot error: Windows Update Triple Fault"
    description="Virtual machine failed to boot due to failed Windows updates "
    infoBubbleText="Virtual Machine failed to boot due to failed Windows updates"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_UPDATE_CONTAINER_CRASH"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Windows Update Installation Capacity
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the operating system is unable to complete a Windows Update (KB) installation.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot displays the Windows logo with a spinning progress indicator. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Azure VM startup is stuck at Windows update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
