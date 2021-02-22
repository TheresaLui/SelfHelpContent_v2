# Check BGP logs

<properties
pageTitle="Check BGP logs"
description="Check BGP logs"
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
articleId="d54403ec-2f2e-4b1b-92f3-28c388ddb494"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Check BGP status between MSEE and Customer/Provider Edge

### Recommended Action

* Ping the peer
* Open Jarvis actions and run "Brooklyn > ExR Diagnostic Operations > Run Ping Command", and input the following:
  * Device Name = *MSEE name*
  * VRF Name = *Add VRF name in case of Private Peering, else leave it blank*
  * Destination IP Address = *BGP Peer (Customer/Provider Edge) IP address*
  * Device Region = *Global/Regional*
