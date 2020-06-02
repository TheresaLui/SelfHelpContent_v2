<properties
    pageTitle="VM boot error: Windows could not complete installation"
    description="Virtual machine failed to boot with the installation error message 'Windows could not complete the installation'."
    infoBubbleText="A boot error occurred your VM during the Windows installation process."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_COULD_NOT_COMPLETE_INSTALLATION"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: Windows could not complete installation

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code 'Windows could not complete the installation'. If you encounter this error message, it means that Azure attempted a first boot of a generalized image but had trouble to completing the sysprep process. In other words, the image is in an undeployable state and cannot be recovered.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Windows could not complete the installation. To install Windows on this computer, restart the installation**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* Unfortunately, the current VM is not able to be fixed, as it is in an undeployable state. You should instead follow the [directions to upload a generalized VHD to Azure to create a new VM](https://docs.microsoft.com/azure/virtual-machines/windows/sa-upload-generalized).

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
