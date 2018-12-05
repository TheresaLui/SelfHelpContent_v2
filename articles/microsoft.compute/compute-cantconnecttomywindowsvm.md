<properties  
	pageTitle="I can't connect to my Windows VM"
	description="I can't connect to my Windows VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ram-kakani,timbasham"
	authorAlias="scotro,tibasham,ramakk"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32511135,32615531,32615526"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public"
/>

# I can't connect to my Windows VM

4 out of 5 customers resolved their VM connectivity issue using the steps listed below.<br>

## **Recommended steps**

1. Access [Serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) of your VM and verify it is running. Review network state and system state in [serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) of your VM by going to command prompt.<br>
2. [Identify common boot errors and solutions for non-bootable VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot)<br>
3. [Validate that your Network Security Group is allowing traffic](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId)<br>
4. [Use Network Watcher to troubleshoot connectivity issues](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId)<br>
5. [Review effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId) to ensure inbound "Allow" NSG rule exists and is prioritized for RDP port(default 3389).<br>
6. [Reset Remote Access to address remote server issues using PowerShell or CLI](http://aka.ms/resetsarmwinremoteaccess)
7. If you are using VPN S2S, RDP to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises.<br>
8. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade.<br>
9. Address Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host.<br>
10. If you're getting an RDP license error, use 'mstsc/admin' as a work around. If needed, uninstall or buy an RDS license.<br>

## **Recommended Documents**

* [Review the RDP troubleshooting guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)<br>
* [Troubleshoot specific Remote Desktop connection errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors)<br>
* [Detailed troubleshooting across network components](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/)<br>
* [Address Remote Desktop License Server error](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense)
