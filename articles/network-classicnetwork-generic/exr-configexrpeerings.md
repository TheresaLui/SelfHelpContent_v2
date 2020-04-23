<properties
	pageTitle="Configure ExpressRoute Peerings"
	description="Configure ExpressRoute Peerings"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32627979"
	resourceTags=""
	productPesIds="15480"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="0504dbbd-eb4f-4f70-b842-b39882e3ea38"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# Configure ExpressRoute Peerings

Note: Azure public peering has been deprecated, and is not available for new ExpressRoute circuits. New Circuits support Microsoft peering and private peering.

You can configure Azure private and/ or Microsoft peering for an ExpressRoute circuit in any order you choose.

## **Recommended Documents**

* Create and modify ExpressRoute peering configuration using [portal](https://docs.microsoft.com/azure/expressroute/expressroute-howto-routing-portal-resource-manager), [PowerShell](https://docs.microsoft.com/azure/expressroute/expressroute-howto-routing-arm), or [CLI](https://docs.microsoft.com/azure/expressroute/howto-routing-cli)
* Configure route filters for Microsoft peering using [portal](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-portal), [PowerShell](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-powershell), or [CLI](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-cli) to consume a subset of supported services
* [Enable and disable ExpressRoute Peering using PowerShell](https://docs.microsoft.com/azure/expressroute/expressroute-howto-reset-peering)
* [Move Public peering to Microsoft peering](https://docs.microsoft.com/azure/expressroute/how-to-move-peering)
* [Verify ExpressRoute Connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview) whether issue is in your Network, Provider Network, or in Microsoft Data Center
