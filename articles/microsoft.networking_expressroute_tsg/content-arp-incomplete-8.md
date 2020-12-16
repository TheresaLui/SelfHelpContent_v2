# ARP incomplete

<properties
pageTitle="ARP incomplete"
description="ARP incomplete"
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
articleId="192a1d03-cff0-4611-ae8b-0dc1dae7cab9"
ownershipId="CloudNet_AzureExpressRoute"
/>

## ARP incomplete between MSEE and Customer/Provider Edge

### Recommended Action

ARP establishes layer 2 connectivity. When you see an issue, the quickest way you can confirm it is from the ARP incomplete insight on ASC. Natively, you can confirm it from routing details (or Dump Routing Info).

* Browse to the ExpressRoute circuit in ASC and click "DumpRoutingInfo" to download this file.
* Open this text file and look for "*ARP Info:*".
* Ensure there is a MAC address next to the customer's BGP peer IP and *not* the text "*incomplete*".

If ASC is down, you may get this information on Jarvis Actions at Brooklyn > ExR Diagnostic Operations > Dump Routing Info.

This is typically due to a Dot1Q/QinQ mismatch between customer and their service provider. Make sure that the customer and provider side configuration is in accordance with VLAN tags on MSEE for this peering (CTAG and STAG). Have the customer diagnose their layer 2 connectivity with the help of provider and try again.

#### Recommended Reading

* [ARP table when on-premises / connectivity provider side has problems](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-troubleshooting-arp-resource-manager#arp-table-when-on-premises--connectivity-provider-side-has-problems) 
* [Azure ExpressRoute: Router configuration samples](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-config-samples-routing#cisco-ios-xe-based-routers)
