# Circuit creation failure

<properties
pageTitle="Circuit creation failure"
description="Circuit creation failure"
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
articleId="4d196dea-54d6-4ec1-96bf-9000211339a4"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Circuit creation fails

### Recommended Steps

Check the following logs:

1. ARM Operations: Check HTTP Request failures. You can find the logs in ASC at Subscription level, under Operations tab. This can also be found in Kusto Scope: @armprod/ARMProd under HTTPIncomingRequests and HTTPOutgoingRequests.
2. NRP Operations: Check NRP failures. This is present on ASC at the specific Circuit level under Operations tab. This can also be found on Jarvis Logs on FrontendOperationEtwEvent table under NRP namespace.
3. Backend Gateway Manager Operations: Check for Gateway Manager failures. You can find the logs in ASC at the specific Circuit level under Operations tab. This can also be found on Jarvis Logs on AsyncWorkerLogsTable table under BrkGWM namespace.

Try to identify the error. If you are not able to identify error from above logs, and need assistance to further isolate, refer to a TA on Teams via Ava.
