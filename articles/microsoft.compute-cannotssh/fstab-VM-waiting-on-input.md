<properties
	pageTitle="Linux VM waiting on input"
	description="Linux VM waiting on input"
	infoBubbleText="fstab issue found"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="craigwiand"
	displayOrder="1"
	articleId="cant-ssh<tbd>"
	diagnosticScenario="CantSSH"
	selfHelpType="resource"
	supportTopicIds="32411835"
	resourceTags="linux"
	productPesIds="15571"
	cloudEnvironments="public"
/>

#We ran diagnostics on your Linux Virtual machine and found an issue

## **Microsoft Azure VM diagnostic information for [VM]<!--($vmname)-->** ##

Microsoft Azure has concluded an investigation of your Virtual Machine (VM) **[vmname]**<!--($vmname)--> in subscription **[SubscriptionId]**<!--($SubscriptionId)-->. We identified that your VM is currently in a inaccessible state due to the fact it is waiting on user to continue the boot process.  This problem is typically due to a problem in the file system table(fstab) file.  

To view more detailed information, see the serial log output in the boot diagnostics blade in the following portal path:

> Virtual Machines > **[VMNAME]** > All settings > Boot diagnostics
   
## Recovery steps ##
To recover the VM, follow these steps:

1. Attach the OS disk to a recovery VM. To do this, the following Azure article , and follow the steps from the beginning up to “Fix issues on original virtual hard disk” section: [Troubleshoot a Linux VM by attaching the OS disk to a recovery VM using the Azure CLI](https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks)

2. After you mount the OS disk as a data disk on the new VM, correct the fstab file using a text editor on the recovery VM. 
3. After the fstab issues are resolved, return to [Troubleshoot a Linux VM by attaching the OS disk to a recovery VM using the Azure CLI](https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-linux-troubleshoot-recovery-disks), and resume at the *Unmount and detach original virtual hard disk* section for steps to recreate the original VM.


## More Information ##
For more detailed information on correcting fstab issues in Azure Linux virtual machines see:
[Azure Linux VM cannot start because of fstab errors](https://support.microsoft.com/en-us/help/3206699)