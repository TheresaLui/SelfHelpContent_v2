<properties
	pageTitle="I cannot connect to my public endpoint after associating NSG to my virtual machine"
	description="Troubleshooting for connectivity issue to public endpoint after associating NSG to VM"
	service="microsoft.network"
	resource="networksecuritygroups"
	authors="radwiv"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I cannot connect to my public endpoint after associating NSG to my virtual machine.

## **Recommended steps**
NSGs by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps.<br>

1. Review the security rules in your NSG.<br>
2. Check if the backend port used in the load balancer rule configuration is in the allow list.<br>
3. If there is no rule to allow the traffic from Internet, add a new rule to allow access to backend port, with source being 'Internet', '*' or a specific public IP address.<br>

## **Recommended documents**

[NSG rules for load balancer endpoints](https://azure.microsoft.com/documentation/articles/virtual-networks-nsg/#load-balancers)<br>
[Troubleshoot deployment issues for creating a new Virtual machine in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)