<properties
    pageTitle="VM boot error: Windows Boot Manager 0xC0000428 Status Invalid Image Hash"
    description="Virtual machine failed to boot due to the Windows Boot Manager menu stating there was an issue with a file's digital signature. Windows Boot Manager displays the status code 0xC0000428, which means 'Status Invalid Image Hash'."
    infoBubbleText="Windows Boot Manager states that a recent hardware or software change might have installed a file that was signed incorrectly or damaged with the info: 'Windows cannot verify the digital signature of this file'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsBootManager-0xC0000428-STATUS_INVALID_IMAGE_HASH"
    diagnosticScenario="windowsbootmanager"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Windows Boot Manager 0xC0000428 Status Invalid Image Hash
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the image that was used to build the VM was a preview image with an expiration date rather than an RTM (Release to Manufacturing) image. Preview images have a designated lifecycle and this error occurs when you have passed the expiration date, meaning the trial of the image is over. You are not able to extend the expiration date of a preview image. Once the preview has expired, the VM will no longer be able to boot.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **0xc0000428** which states that **The digital signature for this file couldn't be verified**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows boot manager error - 0xC0000428 Status Invalid Image Hash](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-boot-error-invalid-image-hash) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
