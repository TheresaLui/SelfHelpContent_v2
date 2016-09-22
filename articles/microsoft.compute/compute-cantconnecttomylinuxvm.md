<properties  
	pageTitle="I can't connect to my Linux VM" 
	description="I can't connect to my Linux VM" 
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32411835"
	resourceTags="linux, redhat"	
	productPesIds="14749"
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
 6. To connect to your VM via SSH, please review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade) to ensure inbound “Allow” NSG rule exists for SSH port(22)
 7. SSH to your VM from Internet will not work with force tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade) <br>
 With force tunneling, all outbound traffic destined to Internet will be redirected to on-premises
  
## **Recommended documents**
[Detailed troubleshooting of SSH errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-ssh-connections/#detailed-troubleshooting-of-ssh-errors) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
