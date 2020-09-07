<properties
	pageTitle="I cannot connect to my public endpoint after associating NSG to my virtual machine"
	description="Troubleshooting for connectivity issue to public endpoint after associating NSG to VM"
	service="microsoft.network"
	resource="networksecuritygroups"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="20184d93-cd41-486d-861c-7b0f8664d9b0"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I cannot connect to my public endpoint after associating NSG to my virtual machine.

## **Recommended Steps**
NSGs by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps:

1. Review the security rules in your NSG
2. Check if the backend port used in the load balancer rule configuration is in the allow list
3. If there is no rule to allow the traffic from Internet, add a new rule to allow access to backend port, with source being 'Internet', '\*' or a specific public IP address

## **Recommended Documents**

* [Diagnose NSG configuration](https://docs.microsoft.com/azure/virtual-network/diagnose-network-traffic-filter-problem)<br>
* [Troubleshoot deployment issues for creating a new Virtual machine in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)
