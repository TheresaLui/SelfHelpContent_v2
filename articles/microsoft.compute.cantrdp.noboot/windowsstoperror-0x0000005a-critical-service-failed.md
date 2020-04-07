<properties
    pageTitle="VM boot error: #0x0000005A Critical Service Failed"
    description="Virtual machine wants to restart due to a critical service failure."
    infoBubbleText="A boot error occurred your VM with the stop code 'CRITICAL SERVICE FAILED'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0x0000005A-CRITICAL_SERVICE_FAILED"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: #0x0000005A Critical Service Failed

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows ran into a problem and needs to restart with the stop code 'CRITICAL SERVICE FAILED'. If you encounter this error message, it usually is due to unsigned drivers. Typically, this will occur after attempting to install a Windows Update KB, but the installation fails. Checking the system log on the latest KB will provide insight into which KB could have caused the problem.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would show Windows ran into a problem and needs to restart with the stop code **CRITICAL SERVICE FAILED**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Critical Service Failed](https://docs.microsoft.comazure/virtual-machines/troubleshooting/troubleshoot-critical-service-failed-boot-error) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
