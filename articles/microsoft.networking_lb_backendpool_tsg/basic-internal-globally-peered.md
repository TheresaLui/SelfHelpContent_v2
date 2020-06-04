<properties
	pageTitle="Basic load balancer support"
	description="Basic load balancer support"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3bab1fde-c04a-4815-9231-50d92fd76bab-globally-peered"
	ownershipId="CloudNet_LoadBalancer"
/>

# Basic load balancer support

* Resources in one virtual network cannot communicate with the front-end IP address of a Basic internal load balancer in a globally peered virtual network.
* Support for Basic Load Balancer only exists within the same region.
* Support for Standard Load Balancer exists for both, VNet Peering and Global VNet Peering.
* Services that use a Basic load balancer which will not work over Global VNet Peering are documented here.
* Advise customer of options to switch to a different load balancer

## **Recommended Documents**

* https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#what-are-the-constraints-related-to-global-vnet-peering-and-load-balancers