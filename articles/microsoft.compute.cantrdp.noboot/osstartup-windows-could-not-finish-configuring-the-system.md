<properties
    pageTitle="VM boot error: Windows could not finish configuring the system"
    description="Virtual machine failed an initial boot of a generalized image while setup is starting services."
    infoBubbleText="A Windows setup error prompt: 'Windows could not finish configuring the system'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_COULD_NOT_FINISH_CONFIGURING_THE_SYSTEM"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Windows could not finish configuring the system
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the VM wasn't able to complete the Sysprep process. This error occurs when attempting an initial boot of a generalized image, which means that the image is in an undeployable state and cannot be recovered.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Windows could not finish configuring the system. To attempt to resume configuration, restart the computer. Setup is starting services**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows could not finish configuring the system](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-could-not-configure-system) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
