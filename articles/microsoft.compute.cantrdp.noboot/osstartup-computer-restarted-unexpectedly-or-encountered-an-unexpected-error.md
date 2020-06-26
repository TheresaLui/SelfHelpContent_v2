<properties
    pageTitle="VM boot error: Computer restarted unexpectedly or encountered an unexpected error"
    description="Virtual machine failed an initial boot of a generalized image due to a custom answer file being processed."
    infoBubbleText="An Install Windows error during initial boot of an image with the message: 'Computer restarted unexpectedly or encountered an unexpected error'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-COMPUTER_RESTARTED_UNEXPECTEDLY_OR_ENCOUNTERED_AN_UNEXPECTED_ERROR"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Computer restarted unexpectedly or encountered an unexpected error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because a custom answer file was processed. Custom answer files are not supported in Azure. This issue is most often created while you are using Sysprep.exe with an on-premises VM to upload a generalized VM to Azure.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Computer restarted unexpectedly or encountered an unexpected error**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Computer restarted unexpectedly or encountered an unexpected error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-unexpected-restart-error-during-vm-boot) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
