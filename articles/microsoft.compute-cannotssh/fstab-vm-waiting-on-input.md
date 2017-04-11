<properties
	pageTitle="VM boot error"
	description="Linux VM waiting on input"
	infoBubbleText="fstab issue has been found"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="craigwiand"
	displayOrder="1"
	articleId="VMCannotSSH_D798E6ED-7353-480D-8825-51C2729DD5BA"
	diagnosticScenario="CantSSH"
	selfHelpType="diagnostics"
	supportTopicIds="32411835"
	resourceTags="linux"
	productPesIds="15571"
	cloudEnvironments="public"
/>

# Diagnostics on your Linux Virtual machine found a boot error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->. We identified that your VM is currently in a inaccessible state because it is waiting on user input to continue the boot process.  This problem is most commonly due to a problem in the file system table(fstab) file.  

To view more detailed information, see the serial log output in the boot diagnostics blade in the following portal path: **Virtual Machines** > <!--$vmname-->**[vmname]**<!--/$vmname--> > **All settings** > **Boot diagnostics**
<!--/issueDescription-->
   
## **Recommended Steps**
To recover the virtual machine, follow these steps:

1. Attach the OS disk to a recovery VM. To do this, review the following Azure article and follow the steps from the beginning up to *Fix issues on original virtual hard disk* section: [Troubleshoot a Linux VM by attaching the OS disk to a recovery VM using the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks).

2. After you mount the OS disk as a data disk on the new VM, correct the fstab file using a text editor on the recovery VM. For more detailed information on correcting fstab issues in Azure Linux virtual machines see:
[Azure Linux VM cannot start because of fstab errors](https://support.microsoft.com/help/3206699).

3. After the fstab issues are resolved, return to [Troubleshoot a Linux VM by attaching the OS disk to a recovery VM using the Azure CLI](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks), and resume at the *Unmount and detach original virtual hard disk* section for steps to recreate the original VM.
