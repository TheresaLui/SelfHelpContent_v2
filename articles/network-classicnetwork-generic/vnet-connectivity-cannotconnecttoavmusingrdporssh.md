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
Follow below steps to resolve common networking related RDP or SSH issues:<br>
1. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.sourceId.$resourceId) to troubleshoot connectivity issues when trying RDP or SSH from Azure.<br>
2. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group is blocking traffic to or from a virtual machine.<br>
3. Review effective security group rules to ensure inbound “Allow” NSG rule exists and is prioritized for RDP or SSH port(default 3389/22).<br>
4. RDP or SSH to your VM from Internet may not work with forced tunneling enabled. With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises. Review effective routes.<br>

## **Recommended documents**
[Steps to address common RDP connection issues](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
[Steps to address common SSH connection issues](https://docs.microsoft.com/azure/virtual-machines/linux/troubleshoot-ssh-connection)
