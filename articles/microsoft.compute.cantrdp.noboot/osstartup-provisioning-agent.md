<properties
    pageTitle="VM boot error: Provisioning Agent"
    description="Virtual machine failed to boot due to improper preparation and now show the error handler."
    infoBubbleText="A boot error occurred your VM and now displays the error handler window during the setup process."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michaeljbuford"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-PROVISIONING_AGENT"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Provisioning Agent
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because SYSPREP was ran on this VM and then the VM was restarted without performing a proper post-provisioning cleanup. ErrorHandler.cmd is part of the IaaS provisioning agent, which should only run when a VM is first provisioned from a generalized image. The cleanup process is responsible for removing the unattend.wsf answer file as well as  unmounting the ISO from the CD-ROM. Since this wasn't performed, it triggers the provisioning agent and remains stuck during setup.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **​Administrator: ERROR HANDLER**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* At this stage the VM is broken. You either need to restore it from backup or to download the VHD and manually finish the out-of-box-experience wizard.

* See recommended documents below for assistance in properly preparing a VHD for upload, generalizing a VM using SYSPREP, or creating a VM from a generalized image.

## **Recommended Documents**

* [Prepare a Windows VHD or VHDX to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)

* [Upload a generalized VHD and use it to create new VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/upload-generalized-managed)

* [How to create an unmanaged VM image from an Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/sa-copy-generalized)

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
