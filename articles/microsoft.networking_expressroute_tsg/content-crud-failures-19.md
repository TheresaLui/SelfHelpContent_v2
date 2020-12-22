# CRUD failures

<properties
pageTitle="CRUD failures"
description="CRUD failures"
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
articleId="a34260c4-11b1-4871-b941-7e57e3bfbe0d"
ownershipId="CloudNet_AzureExpressRoute"
/>

## CRUD (Create/Read/Update/Delete) failure while setting up Peering

The CRUD operation on peering may fail on Azure portal/PowerShell/CLI. You may be able to track these errors in NRP and BRKGWM/BRKGWT namespaces.

### Recommended Action

* Check in ASC > ExpressRoute circuit > Operations > NRP, or  
* Use Jarvis NRP logs [example](https://jarvis-west.dc.ad.msft.net/A67BBF48), or
* Use this Kusto query [example](https://dataexplorer.azure.com/clusters/nrp/databases/mdsnrp?query=H4sIAAAAAAAAA2WOPU7DQBSEe07x5Ca2tEpLQ1KQuHADxvEFNruDY2R7l/fWBEsUXIPrcRLWETIguvcz882YbpQATlcD+1W2tjrooxakSW8lnpJs/eAkD+f8BUO4eqPzCQwqGaYV1G2PQ9C9py3pxqXXNlskh/EohlsfWjcUljYbSm7ER9vjRJMbmUwMdj348/1DSH6pqdjTjNgmC+zeg/X8u9M9LqxyDPmrZ4hUbgy4bXwJcDs0i3R2e3ZPMOFfX0U1Bj0EFWsaEyGKKkhsZVBPHj/bnKf+xivaOWZ0l0OF5xESCqsoZ3a8cxbf4x5Bt92F3ETlF0DKuRRpAQAA)

Look at the "ErrorCode" and "ErrorDetails". Please consider the below actions with respect to the "ErrorCode".
| ErrorCode | Action|
|--|--|
|RetryableError |Look to see if the "ErrorDetails" column indicates the customer subscription reached the throttling limit or if another operation is in progress. If so, instruct the customer to retry the creation.
|InvalidAddressPrefixFormat |Help customer validate the prefix they are specifying valid /30 prefixes for the primary and secondary prefixes. You may refer to [this website](http://www.subnet-calculator.com/cidr.php) to help calculate valid prefixes.
|ParentResourceIsInFailedState |Have customer use Azure PowerShell or Azure Cloud Shell in the Portal. <br> Next, have the customer run *Get-AzExpressRouteCircuit \| Set-AzExpressRouteCircuit*. Ensure circuit is no longer in a failed state. If so, retry the operation. Otherwise, engage your TA.|
|ExpressRoutePrivatePeeringConfigIncomplete |Ensure that the customer provided all the required parameters as publicly documented [here](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-howto-routing-portal-resource-manager).|
|\<Blank> |Look at the "ErrorDetails". If you see the error "The specified bgp shared key length was not valid. The maximum length supported is 25.", refer customer to public documentation [here](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-howto-routing-portal-resource-manager) which explains the 25 alphanumeric character limit. Special characters are not supported. <br> If you see "InternalServerError", ask the customer to retry the operation. If the retry fails, note the "CorrelationRequestId" and timestamp and engage an available TA and escalate case to a CRI. |
