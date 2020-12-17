# Hold timer issues

<properties
pageTitle="Hold timer issues"
description="Hold timer issues"
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
articleId="b7e85f45-de03-44d2-addc-9b944e444188"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Hold timer expired

* This error is very generic which usually comes if a router does not receive successive KEEPALIVE and/or UPDATE and/or NOTIFICATION messages within the period specified in the Hold Time field of the OPEN message, then the NOTIFICATION message with Hold Timer Expired Error Code is sent and the BGP connection closed.  
* This means that there was no BGP messages exchanged between the peers for specified time (Hold down time, by default its 3 minutes).  

### Solution

* Check the connectivity between the BGP peers. Its possible that the link between both the BGP peer was unstable.
* If issue persist then run continuous ping between the peers and check for any packet drops. If this message is seen between MSEE and Customer edge device, then check with customer for link stability from their end.
* In case this message seen between MSEE and Gateway peer, then check for any maintenance on respective Gateway tenants. NetVMA should be a good starting place for this, you can enter deployment id of the Gateway or just enter service key of the circuit and check respective details.
