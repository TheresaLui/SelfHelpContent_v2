<properties pageTitle="I can't connect to my Linux VM"
	description="I can't connect to my Linux VM" 
	service="Microsoft.Compute"
	resource="virtualMachines" 
	documentationCenter=""
	authors="aashu"
	resourceTags="linux"
	selfHelpType="resource"
	supportTopicIds=""
	productPesIds=""
	displayOrder="1" />

# I can't connect to my Linux VM

## **Recommended steps**
To resolve the most common issues, try one or more of the following steps.

2. Review your VM's [console screenshot or logs](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to correct boot problems. Review errors in log such as FSTAB (file systems table), FSCK (file system consistency) or Networking errors.
3. Reset Password to address authentication errors. <br>
   [Reset Password using CLI or PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-troubleshoot-ssh-connection/#fix-common-ssh-errors)	
4. Restart the Virtual Machine to address startup issues. <br>
   Click 'Restart' at the top of the VM resource blade.
5. Address any Azure host issues by redeploying, which will migrate the VM to a new Azure host.<br>
   [Redeploy](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy)
6. Reset SSH configuration to fix any SSH issues.<br>
   [Reset SSH using CLI](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-classic-reset-access/#sshconfigresetcli)

## **Recommended documents**
[Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-troubleshoot-ssh-connection/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)



