<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot becuse it is stuck on the Hyper-V procress."
    infoBubbleText="A boot error occurred because your VM failed to boot becuse it is stuck on the Hyper-V procress."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="BootErrorHYPERV"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM Boot Error

<!--issueDescription-->

We have investigated and determined that your virtual machine is in an inaccessible state because we could not find an operation system.

<!--/issueDescription-->


## **Recommended Steps**

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>

1. Proceed with a redeploy which will move the VM to another host

2. If that is does not resolve the problem, then recreate the VM so it is allocated in a different cluster all together.
