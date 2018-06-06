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

Note:<br>
- Peering status needs to show connected. If the status shows initiated, you may need to create another peering link<br>
- Peerings are not transitive<br>

Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to check if traffic is allowed to or from a virtual machine<br>

## **Recommended documents**
Consider these [constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#a-nameabout-peeringaabout-peering) in peering virtual networks