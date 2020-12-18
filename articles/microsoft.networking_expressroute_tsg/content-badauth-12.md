# BADAUTH

<properties
pageTitle="BADAUTH"
description="BADAUTH"
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
articleId="6f118a54-5f0f-40b8-b8bd-082c7ef65d65"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Authentication failure - BADAUTH/Invalid MD5 digest

This error indicates that the MD5 hash, i.e., the password set while configuring BGP peering is not same between MSEE and CE/CPE, or it's possible that only MD5 hash/password is only set on one side.

### Solution

Please check with the customer and accordingly make sure that the BGP password settings are same on both the ends.

#### Recommended Reading

[Create/Modify ExpressRoute Peering](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-howto-routing-portal-resource-manager)
