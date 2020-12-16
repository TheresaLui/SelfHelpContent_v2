# Prefix exhausted

<properties
pageTitle="Prefix exhausted"
description="Prefix exhausted"
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
articleId="2d2c79a7-2962-4207-9ba0-400cf097b020"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Maximum number of prefixes reached

* This error indicates that the prefixes advertised by the peer device to MSEE reached the maximum capacity.
* We usually see BGP peers as flapping due to this error because once Maximum allowed prefixes reached, then BGP peers get reset.

### Recommended Reading

[Maximum prefixes supported per peering](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-circuit-peerings#peeringcompare)  
| Peering type | Maximum prefixes supported|
|--|--|
| Private Peering | 4000 by default <br> 10,000 with ExpressRoute Premium|
| Microsoft Peering | 200 routes |
| Public peering    | 200 routes |

### Solution

* Customers can limit the route advertisement over the respective peering to avoid BGP down events.  
* Customers can also upscale the circuit SKU (in the case of private peering) to increase the limits.
