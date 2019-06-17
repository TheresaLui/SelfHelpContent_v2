<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because it couldn't configure Windows"
    infoBubbleText="Your virtual machine has stalled on the 'Starting Windows' screen. The operating system is corrupted and you'll need to restart your machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="OSStartUp-OOBE_SQL"
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

1. If the image for the Virtual Machine has Windows SQL 2016 installed, then it is missing a prerequirement. Follow these steps [Install SQL Server with SysPrep](https://msdn.microsoft.com/en-us/library/ee210664.aspx)

)
2. If that fails to address the problem, it is recommended that you escalate this case to [Azure Support](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). This script will create a recovery machine which can be used to further troubleshoot the issue and then swap the disk back to the original problem machine.
.  