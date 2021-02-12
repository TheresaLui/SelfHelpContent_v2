<properties
	pageTitle="connectivity/cannotconnecttoavirtualmachineusingrdporssh"
	description="connectivity/cannotconnecttoavirtualmachineusingrdporssh"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32547225"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="9e942f7e-79cc-420d-ab9b-7888a035f55f"
	ownershipId="CloudNet_VirtualNetwork"
/>

# connectivity/cannotconnecttoavirtualmachineusingrdporssh

## **Recommended Steps**

Follow below steps to resolve common networking related RDP or SSH issues:<br>

1. [Troubleshoot connectivity issues](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.sourceId.$resourceId) when trying RDP or SSH from Azure
2. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group is blocking traffic to or from a virtual machine
3. Review effective security group rules to ensure inbound “Allow” NSG rule exists and is prioritized for RDP or SSH port (default 3389/22)
4. RDP or SSH to your VM from Internet may not work with forced tunneling enabled. With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises. Review effective routes.<br>

## **Recommended Documents**

* [Common RDP connection issues](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)<br>
* [Common SSH connection issues](https://docs.microsoft.com/azure/virtual-machines/linux/troubleshoot-ssh-connection) <br>
* [Solve **VNet Peering** issues - Answer 3 questions](https://support.microsoft.com/help/4486956/troubleshooter-for-virtual-network-peering-issues)
