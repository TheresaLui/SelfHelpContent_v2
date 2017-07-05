<properties
	pageTitle="connectivity/cannotconnecttoavirtualmachineusingrdporssh"
	description="connectivity/cannotconnecttoavirtualmachineusingrdporssh"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32547225"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# connectivity/cannotconnecttoavirtualmachineusingrdporssh

## **Recommended steps**
Follow below steps to resolve common networking related RDP/ SSH issues:<br>
1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to confirm if a rule in a Network Security Group is blocking traffic to or from a virtual machine. You can also review  [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade) to ensure inbound “Allow” NSG rule exists and is prioritized for RDP/ SSH port(default 3389/22)<br>
2. RDP/ SSH to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises<br>

## **Recommended documents**
[Steps to address common RDP connection issues](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
[Steps to address common SSH connection issues](https://docs.microsoft.com/azure/virtual-machines/linux/troubleshoot-ssh-connection)
