<properties
    pageTitle="I cannot connect to my public endpoint after associating NSG to my virtual machine"
    description="Troubleshooting for connectivity issue to public endpoint after associating NSG to VM"
    service="microsoft.network"
    resource="networksecuritygroups"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="9a622df1-5f1b-4bfb-90fe-ab7f88d5d4d9"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I cannot connect to my public endpoint after associating NSG to my virtual machine.

## **Recommended Steps**

By default, Network Security Groups (NSGs) deny connections from the Internet unless it is explicitly allowed. To resolve this issue, try one or more of the following steps:

1. Review the security rules in your NSG
2. Check if the backend port used in the load balancer rule configuration is in the allow list
3. If there is no rule to allow the traffic from Internet, add a new rule to allow access to backend port, with the source being "Internet", "*", or a specific public IP address.

## **Recommended Documents**

* [NSG rules for load balancer endpoints](https://docs.azure.cn/virtual-network/virtual-networks-nsg#load-balancers)<br>
* [Troubleshoot deployment issues for creating a new Virtual machine in Azure](https://docs.azure.cn/virtual-machines/windows/classic/troubleshoot-deployment-new-vm#error-string-lookup)
