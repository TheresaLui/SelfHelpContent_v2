<properties
	pageTitle="Troubleshoot and resolve connectivity issues to Azure Private, Azure Public, or Dynamics 365 Services"
	description="Troubleshoot and resolve connectivity issues to Azure Private, Azure Public, or Dynamics 365 Services"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32627985"
	resourceTags=""
	productPesIds="15480"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="08f1b78e-236c-4715-a81f-1cf91eb1950c"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# Troubleshoot and resolve connectivity issues to Azure Private, Azure Public, or Dynamics 365 Services

ARP entries can help validate layer 2 configuration and help troubleshoot basic layer 2 connectivity issues.

## **Recommended Steps**

* If there is only one entry in the ARP table or the on-premise MAC address shows 'incomplete', first open a support request with your connectivity provider to resolve ARP issues
* Verify ARP entries in [Resource Manager](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-arp-resource-manager) or [Classic](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-arp-classic) Deployment models

## **Recommended Documents**

For Azure Private Peering connectivity issues:

* [Verify ExpressRoute Connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview), whether issue is in your Network, Provider Network, or in Microsoft Data Center
* [Setup test environment to analyze how Azure networking services interoperate](https://docs.microsoft.com/azure/networking/connectivty-interoperability-preface?toc=%2fazure%2fexpressroute%2ftoc.json) at the control plane and data plane levels

For Microsoft Peering (i.e. Azure Public or Dynamics 365 Services) connectivity issues:

* [Configure route filters](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-portal) to consume a subset of services through Microsoft Peering
* [Move a public peering to Microsoft peering](https://docs.microsoft.com/azure/expressroute/how-to-move-peering)
* [Reset](https://docs.microsoft.com/azure/expressroute/reset-circuit) a failed ExpressRoute circuit
