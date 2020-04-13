<properties
    pageTitle="VM boot error: Windows Boot Manager Menu"
    description="Virtual machine failed to boot due to the Windows Boot Manager menu"
    infoBubbleText="A Windows Boot Manager prompt 'Choose an operating system to start, or press TAB to select a tool:'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsBootManager-WINDOWS_BOOT_MANAGER_MENU"
    diagnosticScenario="windowsbootmanager"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Windows Boot Manager menu
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the BCD flag displaybootmenu in the Windows Boot Manager is enabled. When the flag is enabled, Windows Boot Manager prompts the user during the booting process to select which loader they wish to run, causing a boot delay. In Azure, this feature can add to the time it takes to boot a VM.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Windows Boot Manager - Choose an operating system to start, or press TAB to select a tool:r**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows Boot Manager Menu](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-guide-windows-boot-manager-menu) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
