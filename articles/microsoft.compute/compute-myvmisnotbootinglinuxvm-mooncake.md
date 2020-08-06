<properties  
    pageTitle="Resolve a not booting issue with your Linux VM"
    description="Resolve a not booting issue with your Linux VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder="35"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="linux,redhat,Ubuntu"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="compute-myvmisnotbootinglinuxvm-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# Resolve connection issue with your Linux VM

4 out of 5 customers resolved their VM not booting issue using the steps listed below.

## **Recommended Steps**

To resolve common issues, try one or more of the following:

If your Linux virtual machine (VM) is not booting and you are unsure of the cause, you can start by accessing the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) for your VM and determine if the VM is experiencing a boot error.

* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.azure.cn/virtual-machines/troubleshooting/boot-diagnostics) in Azure
* Verify that [Boot Diagnostics](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) are enabled for your VM
* View the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) before continuing to the next section

* Access [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM  and verify if your VM is running. If you prefer, you can also see logs by selecting the Boot Diagnostics menu item under the Support + Troubleshooting sub-header for your virtual machine.
* Review errors in [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM or in logs for errors such as:

    * If your VM is experiencing an issue with the [FSTAB](https://support.microsoft.com/help/3206699/azure-linux-vm-cannot-start-because-of-fstab-errors) file (file systems table)
    * If you VM needs to have the file system consistency checked use [FSCK](https://support.microsoft.com/help/3213321/linux-recovery-cannot-ssh-to-linux-vm-due-to-file-system-errors-fsck)
    * Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host

## **Recommended Documents**

* [Detailed troubleshooting of SSH errors](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-ssh-connection?toc=%2Fazure%2Fvirtual-machines%2Flinux%2Ftoc.json#detailed-troubleshooting-of-ssh-errors)
* [Automate Linux VM Customization Tasks using Custom Script Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
