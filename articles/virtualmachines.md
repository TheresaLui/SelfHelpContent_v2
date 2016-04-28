<properties pageTitle="Sample article" 
	description="This is an example article" 
	services="microsoft.classiccompute, microsoft.compute" 
	documentationCenter=""
	authors="aashu"
	tag="linux, windows" />

# I can't connect to my Linux VM

###Recommended steps
To resolve the most common issues, try one or more of the following steps.

1. Check VM's [Resource Health](data-blade:Microsoft_Azure_Support.ResourceHealthDetailBlade) for any platform issues.
2. Review your VM's [console log](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade) or screenshot to correct boot problems. Review errors in log such as FSTAB (file systems table), FSCK (file system consistency) or Networking errors.
3. [Reset Password](data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade) to address authentication errors.
4. Restart the Virtual Machine to address startup issues. <br>
   Click 'Restart' at the top of the VM resource blade.
5. Resize the VM to fix host issues. <br>
Click 'Size' in the Settings blade of the VM resource.
6. Reset SSH configuration to fix any SSH issues.<br>
   [Reset SSH using CLI](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-classic-reset-access/#sshconfigresetcli)

###Recommended documents
[Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-troubleshoot-ssh-connection/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)



