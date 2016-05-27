<properties 
	pageTitle="I can't connect to my Linux VM" 
	description="I can't connect to my Linux VM" 
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="linux"	
	productPesIds=""
	cloudEnvironments="public" 
/>
    
# I can't connect to my Linux VM
 
## **Recommended steps**
 To resolve common issues, try one or more of the following steps.
 
 1. Review your VM's [console screenshot or logs](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to correct boot problems. Review errors in the logs such as FSTAB (file systems table), FSCK (file system consistency), or networking
 2. Reset Password to address authentication errors <br>
 [Reset Password using CLI or PowerShell](http://aka.ms/resetarmpass)
 3. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
 4. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy), which will migrate the VM to a new Azure host
 5. Reset the SSH connection and configuration to fix SSH issues <br>
 [Reset SSH connection using CLI or PowerShell](http://aka.ms/resetarmssh)
 
## **Recommended documents**
[Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)