<properties  
    pageTitle="Resolve a not booting issue with your Linux VM"
    description="Resolve a not booting issue with your Linux VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds="32675597,32675600,32675601,32675599"
    resourceTags="linux,redhat,Ubuntu"
    productPesIds="15571,16342,16065,15797,16454,16470"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="151455db-1b97-415c-a86e-eb1d23147f3e"
	ownershipId="Compute_VirtualMachines"
/>

# Resolve connection issue with your Linux VM

4 out of 5 customers resolved their VM not booting issue using the steps listed below.

## **Recommended Steps**

To resolve common issues, try one or more of the following:

If your Linux virtual machine (VM) is not booting and you are unsure of the cause, you can start by accessing the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) for your VM and determine if the VM is experiencing a boot error.

* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) in Azure<br>
* Verify that [Boot Diagnostics](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) are enabled for your VM<br>
* View the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) before continuing to the next section

1. Access [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM  and verify if your VM is running. If you prefer, you can also see logs by selecting the Boot Diagnostics menu item under the Support + Troubleshooting sub-header for your virtual machine.
2. Review errors in [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM or in logs for errors such as 
3. If your VM is experiencing an issue with the [FSTAB](https://support.microsoft.com/help/3206699/azure-linux-vm-cannot-start-because-of-fstab-errors) file (file systems table).<br> 
4. If you VM needs to have the file system consistency checked use [FSCK](https://support.microsoft.com/help/3213321/linux-recovery-cannot-ssh-to-linux-vm-due-to-file-system-errors-fsck)<br>
5. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host

## **Recommended Documents**

* [Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
* [Automate Linux VM Customization Tasks using Custom Script Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
* [Troubleshooting a Linux VM that is using LVM and is not booting](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/chroot-logical-volume-manager)
