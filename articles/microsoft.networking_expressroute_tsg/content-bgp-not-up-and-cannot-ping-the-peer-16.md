# BGP NOT UP and CANNOT PING the Peer

<properties
pageTitle="BGP NOT UP and CANNOT PING the Peer"
description="BGP NOT UP and CANNOT PING the Peer"
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
articleId="4952c952-7072-4e1c-a489-822b8b76c052"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Check config and layer 2 connectivity

### Recommended Action

This could be an issue with

1. Layer 1 connectivity with Physical Port or Wiring issues at the provider end.
1. Layer 2 connectivity indicated by Incomplete ARP.
1. Configuration issues with VLAN, STAG, CTAG, Peering IP, etc.

#### Note

Microsoft does not control these scenarios. In the above scenarios, the customer should be advised to refer to his local network team and provider to fix the respective issues.
