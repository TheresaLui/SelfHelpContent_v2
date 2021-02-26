# VNET Linking issues

<properties
pageTitle="VNET Linking issues"
description="VNET Linking issues"
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
articleId="008b431a-b510-470e-bd73-20d29517f3fb"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Unable to link VNet to ExpressRoute Circuit in a Private Peering configuration

### Recommended Action

If you are not able to link a Virtual Network to an ExpressRoute circuit, start by tracking it on Jarvis in:

* Frontend Logs: In NRP > FrontendOperationEtwEvents [(*example reference*)](https://jarvis-west.dc.ad.msft.net/28F1B5B3), look for errors, exceptions, and failures around the same time.
* If you see "InternalServerError" or "Retryable" error or the error is not very descriptive, proceed to check in Gateway Manager log. (Note: *OperationId* in NRP is same as *ActivityId* in GWM)
* Gateway Manager Logs: Similarly, in BrkGWM > AsyncWorkerLogsTable [example reference](https://jarvis-west.dc.ad.msft.net/26AC8D45), look for errors and exceptions.

If you see following errors/exception, then please review the respective actions.
|Error/Exception |Action |
|--|--|
|SubnetOverlapsWithExistingAddressSpaceException |Please check more details of this exception. This error indicates that the VNET which customer is trying to link has overlap address spaces with existing connections on the same circuit.<br>Make sure that there are no overlaps and then retry the operation.<br>If issue persists, please engage an available TA via Ava. |
|There was no endpoint listening at https://*\<ER GW VIP>*:8443/ |This issue indicates that GWM was unable to communicate with the GWT hence the required changes were not configured on GWT.<br>A UDR or NSG on GW subnet is most common cause of this problem.<br>Make sure there is no NSG or UDR on GW subnet which blocks the communication. If still there are issues, please reach out to TAs via Ava.?|
|Unable to configure devices: \<MSEE-1>(Success), \<MSEE-2>(Failure) |When GWM unable to configure the MSEE devices then we will see Failure against the specific MSEE device. Usually, this error comes when the respective MSEE device is not reachable due to some planned maintenance/activity. <br>Check for any planned activity on the MSEE device for which you see failure.<br>If there are no planned activity then retry the operation after some time. <br>If we still see the failure, then please engage TAs for further help. |
