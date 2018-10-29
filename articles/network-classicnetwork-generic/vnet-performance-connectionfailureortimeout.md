<properties
	pageTitle="performance/connectionfailureortimeout"
	description="performance/connectionfailureortimeout"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32547228"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# performance/bandwidthorlatencyissue

## **Recommended steps**
1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to check if traffic is allowed to or from a virtual machine<br>
2. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade.id.$subscriptionId) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>
3. Use [Security group view](data-blade:microsoft_azure_network.networkwatchersecuritygroupviewblade.id.$subscriptionId) to see NSGs and rules associated at a NIC and subnet level for VM<br>

## **Recommended documents**
* [Understand outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)
