<properties
	pageTitle="configurationandsetup/howtocreaterulesinanexistingnsg"
	description="configurationandsetup/howtocreaterulesinanexistingnsg"
	infoBubbleText="Common Solutions Template"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="damendo"
	ms.author="damendo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584257"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="9e12c5bc-79c3-4f5c-b5ef-0f68f7d8f9e7"
	ownershipId="CloudNet_VirtualNetwork"
/>

# configurationandsetup/howtocreaterulesinanexistingnsg

[Azure Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview) provides tools to monitor, diagnose, view metrics, and enable or disable logs for resources in an Azure virtual network.

## **Recommended Steps**

1. Organize your network resources with [Network Security Groups (NSGs)](https://docs.microsoft.com/azure/virtual-network/security-overview)
2. Filter traffic coming in and out of your NSG with [Security Rules](https://docs.microsoft.com/azure/virtual-network/security-overview#security-rules) on your NSGs
3. View the Security Rules applied to a an existing Virtual Machine with [Effective Security Rules](https://docs.microsoft.com/azure/network-watcher/network-watcher-security-group-view-overview)
4. Log all the traffic going in and out of your NSG with [NSG Flow Logs](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-overview)
5. Capture traffic on individuals Virtual Machines with [Packet Capture](https://docs.microsoft.com/azure/network-watcher/network-watcher-packet-capture-overview)

In case you are already using Network Watcher tools like NSG Flow Logs, Packet Capture, etc. and have issues/questions about the same, please select the correct topic as below for more detailed help.

1. Azure Portal > Help & Support > Technical > Select your subscription > Select "All services" >
2. Under "Networking" select "Network Watcher" > Select Problem Type as appropriate

## **Recommended Documents**

* [Create rules in an existing NSG](https://docs.microsoft.com/azure/virtual-network/virtual-networks-create-nsg-arm-pportal#create-rules-in-an-existing-nsg)<br>
* [Configure/Enable flow logs for NSG](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal)<br>
* [Read NSG flow logs](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)<br>
* [Azure Security best practices](https://docs.microsoft.com/azure/security/azure-security-network-security-best-practices)<br>
* [Azure Network Security overview](https://docs.microsoft.com/azure/security/azure-network-security)<br>
* [Microsoft cloud services and network security](https://docs.microsoft.com/azure/best-practices-network-security?toc=%2fazure%2fsecurity%2ftoc.json)<br>
* [Reference Architecture: Secure DMZ](https://docs.microsoft.com/azure/architecture/reference-architectures/dmz/secure-vnet-dmz)
