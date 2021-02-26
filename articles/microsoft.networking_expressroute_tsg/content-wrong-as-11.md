# Wrong AS

<properties
pageTitle="Wrong AS"
description="Wrong AS"
service="Microsoft.Network"
resource="Microsoft.Network/expressRouteCircuits,Microsoft.Network/expressRouteCrossConnections,Microsoft.Network/expressRouteGateways,Microsoft.Network/expressRoutePorts,Microsoft.Network/expressRoutePortsLocations,Microsoft.Network/expressRouteServiceProviders"
authors="riturajc"
ms.author="riturajc, assandu"
displayOrder=""
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
articleId="5c17fde4-b714-492d-9f5e-5316426dcb33"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Bad Peer AS - peer in wrong AS

* The error indicates that the ASN configured on MSEE as peer ASN is not same as the local ASN on CPE/PE device.

### Recommended Action

* Verify the BGP configuration at PE/CPE. Please ensure that the peer ASN is configured as Local ASN on CPE/PE.
* If customer by mistake gave wrong ASN while configuring the ExpressRoute peering, then they need to recreate the peering with correct Peer ASN. 

### Recommended Reading

[Create and modify ExpressRoute peering](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-howto-routing-portal-resource-manager)
