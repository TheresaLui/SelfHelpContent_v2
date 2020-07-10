<properties
	pageTitle="Connectivity to Office 365 Services"
	description="Connectivity to Office 365 Services"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32627988"
	resourceTags=""
	productPesIds="15480"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="e428f83f-2175-43fb-b2c6-383f8d9df88d"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# Connectivity to Office 365 Services

ARP entries can help validate layer 2 configuration and help troubleshoot basic layer 2 connectivity issues.

## **Recommended Steps**

 * If there is only one entry in the ARP table or the on-premise MAC address shows 'incomplete', first open a support request with your connectivity provider to resolve ARP issues
* Verify ARP entries in [Resource Manager](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-arp-resource-manager) or [Classic](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-arp-classic) Deployment models

## **Recommended Documents**

* [Configure route filters](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-portal) to consume a subset of services through Microsoft Peering
* Learn about [asymmetric routing](https://docs.microsoft.com/azure/expressroute/expressroute-asymmetric-routing) issues with multiple network paths
* [NAT requirements](https://docs.microsoft.com/azure/expressroute/expressroute-nat) for ExpressRoute setup
* [Verifying ExpressRoute Connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview)
