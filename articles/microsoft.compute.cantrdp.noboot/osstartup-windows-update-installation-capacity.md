<properties
    pageTitle="VM boot error: Windows Update Installation Capacity"
    description="Virtual machine failed to boot due to "
    infoBubbleText="A Windows Boot Manager prompt 'Choose an operating system to start, or press TAB to select a tool:'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_UPDATE_INSTALLATION_CAPACITY"
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
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the operating system is unable to complete a Windows Update (KB) installation, as a core file cannot be created on the file system. Based on this error code, the operating system is unable to write any files to the disk.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot displays Windows Update (KB) in progress, but failing with the error code: `C01A001D`. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows Update installation capacity](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-update-installation-capacity) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
