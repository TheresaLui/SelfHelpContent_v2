# Admin shutdown

<properties
pageTitle="Admin shutdown"
description="Admin shutdown"
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
articleId="2bad727a-bd80-458b-9cb3-efe71479517a"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Administrative shutdown

Administrative shutdown could be of two types:

* Received from neighbor (Administrative Shutdown)
* Sent to neighbor (Administrative Shutdown)

The administrative shutdown indicates that BGP was manually shut down. It usually happens when there is some maintenance activity on either MSEE or CE/PE device.

If we received Administrative shutdown from a peer, this indicates that the peer administratively brings down the BGP.

In case there is some maintenance on MSEE, then MSEE will send BGP notification to PE/CPE specifying "Admin shutdown".

### Solution

* If it is an administrative shutdown due to CE/PE end, then please let customer know about it and ask them to check as if there is any activity going on due to which the peer is Admin down from respective PE/CE. 
* In case we see MSEE is having Admin shutdown, then it could be due to an activity at our end. Please check for any existing ICM, if not sure check with TAs for any planned activity on that MSEE. 
* The next step would be to verify if the BGP peering between second MSEE and CPE/PE is UP, as this would guarantee SLA. We also highly recommend customers to use active-active peering to avoid a single point of failure.


