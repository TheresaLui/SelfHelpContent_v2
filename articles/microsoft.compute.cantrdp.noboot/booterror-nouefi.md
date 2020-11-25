<properties
    pageTitle="VM boot error: No UEFI"
    description="Virtual machine failed to boot and displays No UEFI-compatible file system was found."
    infoBubbleText="Virtual machine failed to boot and displays No UEFI-compatible file system was found."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="BootError-NoUEFI"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: No UEFI

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error **No UEFI-compatible file system was found**, **The boot loader did not load an operating system**. If you encounter this error message, it means that the VHD generation does not match with the generation of the VM.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error **No UEFI-compatible file system was found**, **The boot loader did not load an operating system**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. Resize the VM to a size that supports Generation 1
1. Delete and recreate the VM using a size that supports Generation 1

To determine which VM sizes only support Generation 2 see [Support for generation 2 VMs on Azure](https://docs.microsoft.com/azure/virtual-machines/generation-2).

## **Recommended Documents**

* [VM Sizes in Azure](https://docs.microsoft.com/azure/virtual-machines/sizes)
* [Support for generation 2 VMs on Azure](https://docs.microsoft.com/azure/virtual-machines/generation-2)
