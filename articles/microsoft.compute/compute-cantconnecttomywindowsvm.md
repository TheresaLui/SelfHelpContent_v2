<properties  
	pageTitle="I can't connect to my Windows VM"
	description="I can't connect to my Windows VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32411835"
	resourceTags="windows, windowsSQL"
	productPesIds="14749"
	cloudEnvironments="public"
/>

# I can't connect to my Windows VM

##**Recommended steps**
To resolve common issues, try one or more of the following steps.

1. Verify if your VM is running by viewing your VM's [console screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade)
2. Click here [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to ensure that Network Security Group is allowing traffic
3. Review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade) to ensure inbound “Allow” NSG rule exists and is prioritized for RDP port(default 3389)
4. Reset Remote Access to address remote server issues <br>
[Reset remote access using PowerShell or CLI](http://aka.ms/resetsarmwinremoteaccess)
5. If you are using VPN S2S, RDP to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises
6. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade
7. Address Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy), which will migrate the VM to a new Azure host
8. If you're getting an RDP license error, use 'mstsc/admin' as a work around. If needed, uninstall or buy an RDS license. <br>
[Address Remote Desktop License Server error](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense)

##**Recommended documents**
[Troubleshoot specific Remote Desktop connection errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors) <br>
[Detailed troubleshooting across network components](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/)
