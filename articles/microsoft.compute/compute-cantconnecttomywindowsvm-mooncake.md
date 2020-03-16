<properties  
	pageTitle="I can't connect to my Windows VM"
	description="I can't connect to my Windows VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="windows, windowsSQL"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="a600405f-eef8-4f6f-be12-d8b3cb4f7bbc"
	ownershipId="Compute_VirtualMachines"
/>

# I can't connect to my Windows VM

## **Recommended steps**

To resolve common issues, try one or more of the following steps:<br>

1. Verify if your VM is running by viewing your VM's [console screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId)<br>
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic<br>
3. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$resourceId) to troubleshoot connectivity issues when trying RDP from Azure<br>
4. Review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId) to ensure inbound "Allow" NSG rule exists and is prioritized for RDP port(default 3389)<br>
5. [Reset Remote Access to address remote server issues using PowerShell or CLI](https://docs.azure.cn/virtual-machines/windows/troubleshoot-rdp-connection#fix-common-remote-desktop-errors)<br>
6. If you are using VPN S2S, RDP to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId) With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises<br>
7. Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade<br>
8. Address Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId), which will migrate the VM to a new Azure host<br>
9. If you're getting an RDP license error, use 'mstsc/admin' as a work around.
10. Review[Address Remote Desktop License Server error](https://docs.azure.cn/virtual-machines/windows/troubleshoot-specific-rdp-errors#rdplicense)

## **Recommended documents**

* [Troubleshoot specific Remote Desktop connection errors](https://docs.azure.cn/virtual-machines/windows/troubleshoot-rdp-connection)<br>
* [Detailed troubleshooting across network components](https://docs.azure.cn/virtual-machines/windows/detailed-troubleshoot-rdp/)
