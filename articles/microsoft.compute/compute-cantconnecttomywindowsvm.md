<properties 
	pageTitle="I can't connect to my Windows VM" 
	description="I can't connect to my Windows VM" 
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="windows"	
	productPesIds=""
	cloudEnvironments="public" 
/>
    
# I can't connect to my Windows VM

###**Recommended steps**
To resolve common issues, try one or more of the following steps.

1. Review your VM's [console screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to correct boot problems
2. Reset Remote Access to address remote server issues <br>
[Reset remote access using PowerShell or CLI](http://aka.ms/resetsarmwinremoteaccess)
3. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
4. Address Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy), which will migrate the VM to a new Azure host
5. If you're getting an RDP license error, use 'mstsc/admin' as a work around. If needed, uninstall or buy an RDS license. <br>
[Address Remote Desktop License Server error](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense)

###**Recommended documents**
[Troubleshoot specific Remote Desktop connection errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors) <br>
[Detailed troubleshooting across network components](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/)