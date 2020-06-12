<properties
    pageTitle="VM boot error: Generic Blue Screen"
    description="Virtual machine failed to a generic blue screen error."
    infoBubbleText="A blue screen error stating that 'We're just collecting some error info, and then we'll restart for you'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-BLUESCREEN_GENERIC"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Generic Blue Screen
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state. This may be due to many reasons, such as a corrupted system file or memory, driver issues, or an application a forbidden sector of the memory.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would be a blue screen with the error code **Your PC ran into a problem and needs to restart**. It may additionally state that **We're just collecting some error info, and then we'll restart for you**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows shows blue screen error when booting an Azure VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-common-blue-screen-error) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
