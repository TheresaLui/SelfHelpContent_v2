<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot with error code 0xc0000102"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="WindowsBootManager-0xC0000102-STATUS_FILE_CORRUPT_ERROR"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Windows Boot Manager 0xC0000102 Status File Corrupt Error
<!--issueDescription-->
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->[vmname]<!--/$vmname-->. We identified that your VM is currently in an inaccessible state because Windows failed to boot with error code **0xc0000102**. This issue occurs when a critical system file or the disk file system contain errors.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **0xc0000102** which states that **The operating system couldn't be loaded because a critical system driver is missing or contains errors**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows boot manager error - 0xC0000102 Status File Corrupt](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/error-code-0xc0000102-status-file-corrupt) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
