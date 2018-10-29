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
* Can't connect to a gateway via VNets that are globally peered? Globally peered VNets do not currenly support gateway transit. Read about [VNet peering and Global VNet Peering constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#requirements-and-constraints) <br>
* Can't connect to a load balancer in a globally peered virtual network? This is not currently supported across virtual networks that are globally peered. Read about [VNet peering and Global VNet Peering constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#requirements-and-constraints) <br>
* [Troubleshoot your Network Virtual Appliance (NVA)](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)<br>
* Find answers in [FAQ for VNet Peering](https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#vnet-peering)
