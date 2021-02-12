<properties
    pageTitle="Windows Stop Error: #0x000000EF 'Critical Process Died'"
    description="Virtual machine failed to boot with the stop code 'CRITICAL PROCESS DIED' and now Windows wants to restart automatically."
    infoBubbleText="A Windows stop code 'CRITICAL PROCESS DIED' has been found while booting your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0x000000EF-CRITICAL_PROCESS_DIED"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Windows Stop Error: 'Critical Process Died' while booting a VM
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with stop code 'CRITICAL PROCESS DIED'. If you encounter this error message, it typically means that a critical system process failing during boot, possibly due to OS file corruption.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Your PC ran into a problem and needs to restart. We're just collecting some error info, and then we’ll restart for you. (##% complete) Stop code: CRITICAL PROCESS DIED**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows Stop Error #0x000000EF "Critical Process Died"](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-guide-critical-process-died) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
