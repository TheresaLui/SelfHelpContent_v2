<properties
    pageTitle="VM boot error: 0xC000021A Status System Process Terminated"
    description="Virtual machine failed to boot due to either the WinLogon or Client Server Run-Time Subsystem fails, resulting in a Windows stop error."
    infoBubbleText="A Windows stop error prompt 'Your PC ran into a problem and needs to restart. We're just collecting some error info, and then you can restart' with the error code 0xC000021A."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0xc000021A-STATUS_SYSTEM_PROCESS"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: 0xC000021A Status System Process Terminated
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the either the WinLogon (winlogon.exe) or the Client Server Runtime Subsystem (csrss.exe) failed. These services are critical processes, so when the kernel detects either has stopped, it results in the 0xC000021A error.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **0xC000021A**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows stop error #0xC000021A Status System Process Terminated](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-stop-error-system-process-terminated) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)

* [Bug Check 0xC000021A: WINLOGON_FATAL_ERROR](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-0xc000021a--winlogin-fatal-error)
