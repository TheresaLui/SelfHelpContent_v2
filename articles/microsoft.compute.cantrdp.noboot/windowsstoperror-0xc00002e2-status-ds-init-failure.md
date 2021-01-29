<properties
    pageTitle="VM boot error: Directory Service Initialization Failure"
    description="Virtual machine failed to boot because the Active Dirtectory domain controller cannot be accessed to authenticate user logins. The Local Security Authentication Server will automatically force a restart."
    infoBubbleText="Your PC ran into a problem with the code: 0xC00002E1 or 0xC00002E2"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0xC00002E2-Status_DS_Init_Failure"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Directory Service Initialization Failure
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the Local Security Authentication Server (LSASS.exe) cannot authenticate user logins with Active Directory (AD), which forces a restart. There are multiple reasons why Active Directory may be unnaccessible.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **0xC00002E1** "STATUS_DS_CANT_START", or **0xC00002E2** "STATUS_DS_INIT_FAILURE". This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows stop error - directory service initialization failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-directory-service-initialization-failure) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
