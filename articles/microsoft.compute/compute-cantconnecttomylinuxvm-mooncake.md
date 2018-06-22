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
	cloudEnvironments="MoonCake"
/>

# I can't connect to my Linux VM

## **Recommended steps**
 To resolve common issues, try one or more of the following steps.

 1. Verify if your VM is running by viewing your VM's [console screenshot or logs](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade). Review errors in the logs such as FSTAB (file systems table), FSCK (file system consistency), or networking
 2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade) to ensure that Network Security Group is allowing traffic
 3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade) to troubleshoot connectivity issues when trying SSH from Azure
 4. Review effective security group rules to ensure inbound “Allow” NSG rule exists and is prioritized for SSH port(default 22)
 5. Reset Password to address authentication errors <br>
 [Reset Password using CLI or PowerShell](https://docs.azure.cn/virtual-machines/linux/troubleshoot-ssh-connection#fix-common-ssh-errors/)
 6. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
 7. Reset the SSH connection and configuration to fix SSH issues <br>
 [Reset SSH connection using CLI](https://docs.azure.cn/virtual-machines/linux/troubleshoot-ssh-connection#fix-common-ssh-errors/)
 8. SSH to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises
 9. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel), which will migrate the VM to a new Azure host

## **Recommended documents**
[Detailed troubleshooting of SSH errors](https://docs.azure.cn/virtual-machines/linux/detailed-troubleshoot-ssh-connection/) <br>
[Automate Linux VM Customization Tasks Using CustomScript Extension](https://azure.microsoft.com/blog/automate-linux-vm-customization-tasks-using-customscript-extension/)
