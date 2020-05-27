<properties
	pageTitle="ADFS and SharePoint connections fail behind load balancer over VPN"
	description="Troubleshoot ADFS and SharePoint connection failures behind load balancer over virtual network"
	service="microsoft.network"
	resource="loadbalancers"
	category="Connectivity"
	searchTags=""
	authors="radwiv"
	ms.author="radwiv"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="023f725e-1d77-4f07-a760-f2b706725bf3"
	ownershipId="CloudNet_LoadBalancer"
/>

# ADFS and SharePoint connections fail behind load balancer over VPN

## **Recommended Steps**

1. Adjust ADFS servers’ Maximum Transmission Unit (MTU) to 1350 instead of relying on Path MTU Discovery (PMTUD) as the Internal Load Balancer (ILB) doesn't support PMTUD pass-through
2.	Use a 3rd party network appliance for load balancing (available in Azure portal)
3.	Use an External Load Balancer (ELB/ SLB) instead of the ILB to move this traffic out of the VPN, hence not hitting the MTU restriction
