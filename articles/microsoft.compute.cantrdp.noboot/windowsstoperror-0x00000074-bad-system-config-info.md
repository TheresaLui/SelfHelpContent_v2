<properties
    pageTitle="VM boot error: #0x00000074 Bad System Configuration Info"
    description="Virtual machine failed to boot and needs to restart Windows, which displays the stop code 0x00000074 or 'BAD SYSTEM CONFIG INFO'."
    infoBubbleText="A message stating your PC ran into a problem and needs to restart with the stop code 0x00000074 or 'BAD SYSTEM CONFIG INFO'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0x00000074-BAD_SYSTEM_CONFIG_INFO"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: #0x00000074 Bad System Configuration Info
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because either the system hive is corrupted or if some critical registry keys and values are missing. Hive corruption is unlikely to be the cause, since the boot loader checks for corruption when it loads the hive. Missing registry keys and values is the most likely cause, which may have been due to a user manually editing the registry, or if an application or service has corrupted it.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would show the message **Your PC ran into a problem and needs to restart. You can restart**. <br><br>You should also see the stop code: **BAD_SYSTEM_CONFIG_INFO** or **0x00000074**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows stop error - 0x00000074 Bad System Config Info](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-stop-error-bad-system-config-info) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
