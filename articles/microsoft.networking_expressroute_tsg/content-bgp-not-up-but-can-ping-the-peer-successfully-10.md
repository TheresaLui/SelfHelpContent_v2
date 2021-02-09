# BGP NOT UP but CAN PING the Peer Successfully

<properties
pageTitle="BGP NOT UP but CAN PING the Peer Successfully"
description="BGP NOT UP but CAN PING the Peer Successfully"
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
articleId="78b3c0a4-0504-4519-b78d-8bc682aaef31"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Check current BGP logs from MSEE

### Recommended Action

* Check current BGP logs from MSEE. To do this, open Jarvis actions and run Brooklyn > ExR Diagnostic Operations > Run Show Command. Input the following:  
  * Device Name = \<MSEE name> 
  * Command: show log | include \<BGP peer IP address>  
  * Device Region = Global/Regional  
* Alternatively, you can also search **Syslog** table. Example queries *(replace with respective Timestamp, Device Name and filter with VRF name or Peer IP address)* :
  * [Kusto query example](https://dataexplorer.azure.com/clusters/aznwnetmon/databases/aznwmds?query=H4sIAAAAAAAAAwuuLM7JT+eqUSjPSC1KVQgoSk3OLE4NycxNDS5JzC1QsFNITM/XMM3VhCtxSS3LTE5VsLVVUKqoqNDNywORIGyopJBfhFvaSElBX78otSAnEShdnlmSoVCSkaqQAlFekJhZBACyjtm+iwAAAA==)  
  * [Jarvis Logs example](https://jarvis-west.dc.ad.msft.net/logs/dgrep?page=logs&be=DGrep&offset=-1&offsetUnit=Minutes&UTC=true&ep=Diagnostics%20PROD&ns=NetMon&en=Syslog&conditions=[["Device","contains",""]]&chartEditorVisible=true&chartType=Line&chartLayers=[["New%20Layer",""]]%20)
