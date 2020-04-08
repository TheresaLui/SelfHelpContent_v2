<properties
    pageTitle="VM boot error: Out-of-Box-Experience (OOBE)"
    description="Virtual machine failed to boot because the Out-of-Box-Experience screen is waiting for user input."
    infoBubbleText="A boot error occurred your VM causing the Out-of-Box-Experience to prompt the user to setup Windows."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michaeljbuford"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-OOBE"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: Out-of-Box-Experience (OOBE)

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> failed to boot because the Windows Out-of-Box-Experience (OOBE) is waiting for user input. If you encounter the Out-of-Box-Experience, there are multiple possible reasons, but typically this is due to SysPrep failing, not completing its process, or potentially an issue with improper image generalization.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the OOBE screen will be displayed and will prompt the user for input. The OOBE screen varies depending upon the version of Windows you are running, but will typically display basic setup questions such as the region, language, and keyboard layout. This may also help you diagnose future issues and determine if a boot error is the cause.<br>


## **Recommended Steps**

* [Create a nested virtualization environment](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-vm-by-use-nested-virtualization) to mount the OS disk snapshot and complete the OOBE process. Once you have completed the OOBE process, you may proceed with Step 3 in the nested virtualization guide to rebuild your original VM.

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
