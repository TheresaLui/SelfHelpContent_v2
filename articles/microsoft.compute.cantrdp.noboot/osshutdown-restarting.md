<properties
    pageTitle="VM boot error - Restarting"
    description="Virtual machine failed to boot with message Restarting on screenshot"
    infoBubbleText="Virtual machine failed to boot with message Restarting on screenshot"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="OSShutDown-RESTARTING"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is not booting and shows "Restarting" on the screenshot.  Windows uses the shutdown process to perform system maintenance operations and proceed with changes on the system such as binaries updates and/or roles/features changes. This process is critical and shouldn't be interrupted until it completes. If this process is stopped, it is very likely that the OS will become corrupted. To determine why the service is hung, a memory dump of the process needs to be collected.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the text "Restarting". This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [VM is stuck on shutdown - Restarting](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot-windows) troubleshooting guide
