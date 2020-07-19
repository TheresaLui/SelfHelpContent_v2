<properties
	pageTitle="I am unable to connect to virtual machines in the same VNet when using an UDR."
	description="Troubleshoot connectivity to VM in the same VNet when using an UDR"
	service="microsoft.network"
	resource="routetables"
	authors="radwiv"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="406bbd29-d856-402f-91a1-8a3a2728ca47"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I am unable to connect to virtual machines in the same VNet when using an UDR.

## **Recommended steps**
If you are using User defined routes in your virtual network subnets and have connectivity issues, try one or more of the below steps to resolve the issue.<br>

1. Check the route entries to ensure the destination address you are having issues with is covered by one or more routes. Communication within the Virtual network, to on-premises and to Internet is covered by system routes.<br>
[User defined routes overview](https://azure.microsoft.com/documentation/articles/virtual-networks-udr-overview/)
2. Check that the destination is reachable from other sources.<br>
3. Check that the Network security group rules on both source and destination allow this traffic.<br>
4. If you are using a NVA to route the traffic through, check that the NVA VM is running and 'IP Forwarding' is enabled.<br>
5. Check to validate that NVA is not in the same subnet as the source virtual machine. This will create a route loop.<br>

## **Recommended documents**

[User defined routes design considerations](https://azure.microsoft.com/documentation/articles/best-practices-network-security/#examples-building-security-boundaries-with-azure-virtual-networks)