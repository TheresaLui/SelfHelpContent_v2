<properties
    pageTitle="I am unable to connect to virtual machines in the same VNet when using an UDR."
    description="Troubleshoot connectivity to VM in the same VNet when using an UDR"
    service="microsoft.network"
    resource="routetables"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="332fc705-a89e-461c-b7f0-227bd20b3a58"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I am unable to connect to virtual machines in the same VNet when using an UDR.

## **Recommended Steps**

If you are using User defined routes in your virtual network subnets and have connectivity issues, try one or more of the following steps to resolve the issue:

1. Check the [route entries](https://docs.azure.cn/virtual-network/virtual-networks-udr-overview/) to ensure the destination address you are having issues with is covered by one or more routes. Communication within the Virtual network, to on-premises, and to the Internet is covered by system routes.
2. Check that the destination is reachable from other sources
3. Check that the Network security group rules on both source and destination allow this traffic
4. If you are using a NVA to route the traffic through, check that the NVA VM is running and 'IP Forwarding' is enabled
5. Check to validate that NVA is not in the same subnet as the source virtual machine, as this will create a route loop

## **Recommended Documents**

* [User defined routes design considerations](https://azure.microsoft.com/documentation/articles/best-practices-network-security/#examples-building-security-boundaries-with-azure-virtual-networks)
