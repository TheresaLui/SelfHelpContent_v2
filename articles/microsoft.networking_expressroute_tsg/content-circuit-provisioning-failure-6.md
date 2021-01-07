# Circuit provisioning failure

<properties
pageTitle="Circuit provisioning failure"
description="Circuit provisioning failure"
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
articleId="968d5f3b-695b-45d3-bf69-7158e58e0c01"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Circuit has been created but not yet provisioned

### Recommended Steps

1. Confirm with the provider that the circuit has been provisioned from their end.
2. Check on the ASC whether "Service Provider Provisioning State" is set to "Provisioned" at the specific Circuit level under Properties tab.
3. On the Jarvis Logs at BrkGWM/AsyncWorkerLogsTable, look for operation "UpdateCrossConnectionWorkItem". Search for "ProvisioningError".
4. On the Jarvis Logs at BrkGWM/CircuitEventTable, for a successful provisioning this message is displayed: "Update Cross Connection Operation:NotifyCrossConnectionProvisioned".
