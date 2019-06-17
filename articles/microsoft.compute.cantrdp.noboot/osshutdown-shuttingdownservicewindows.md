<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because it couldn't configure Windows"
    infoBubbleText="Your virtual machine has stalled on the 'Starting Windows' screen. The operating system is corrupted and you'll need to restart your machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="OSShutDown-SHUTTING_DOWN_SERVICE_WINDOWS_MODULES_INSTALLER"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operation system.

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**

1. Force a restart of the Virtual Machine from the portal


 



2. If this is a recurrent issue on every restart causing a slow shutdown operation, then collect a memory dump while the problem is happening and create a support case providing the memory dump collected.