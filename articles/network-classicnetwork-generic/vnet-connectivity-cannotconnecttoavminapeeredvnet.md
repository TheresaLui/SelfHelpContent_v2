<properties
	pageTitle="connectivity/cannotconnecttoavirtualmachineinapeeredvnet"
	description="connectivity/cannotconnecttoavirtualmachineinapeeredvnet"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584249"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# connectivity/cannotconnecttoavirtualmachineinapeeredvnet

**Please Note:**<br>
* Peering status needs to show connected. If the status shows initiated, you may need to create a peering link from the other Vnet<br>
* Peerings are not transitive<br>

## **Recommended steps**
1. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.sourceId.$resourceId) to troubleshoot connectivity issues<br>
2. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to check if traffic is allowed to or from a virtual machine<br>

## **Recommended documents**
[Troubleshoot your **Network Virtual Appliance (NVA)**](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)<br>
[Solve **VNet Peering** issues - Answer 3 questions](https://internal.support.services.microsoft.com/help/4486956/troubleshooter-for-virtual-network-peering-issues) <br>
Consider these [constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#a-nameabout-peeringaabout-peering) in peering virtual networks <br>
Find answers in [FAQ for Vnet Peering](https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#vnet-peering)