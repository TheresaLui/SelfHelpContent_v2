# Route filter issues

<properties
pageTitle="Route filter issues"
description="Route filter issues"
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
articleId="e2586517-139d-4dc3-94f7-600be08c1d41"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Unable to add/remove route filters for Microsoft Peering

* A Route Filter is a way to consume only a subset of supported services through Microsoft peering.
* We may see the add/delete/update route filter operation may fail.
* To proceed, determine the NRP error with this [Kusto query example](https://dataexplorer.azure.com/clusters/nrp/databases/mdsnrp?query=H4sIAAAAAAAAA32PTU7DMBCF95xilE0TyeqWDe2mDVI2/LS5gGtPi1Fim5kJVSSEuAbX4yS4bqVSgdjZo/e+957pBhakcuIpTqqp1aI3mrEsesvpVFTTx8C17OtX9AJw9Qb7JySEB0LjGFvX41p0H2EOehfKa1udNethw4ZcFBd8Y2E2g+KGY/JtRxjDQGBSduiRvj4+GfiHGpolHBDz4kxbISePwXaMmFkUBsFb16X6/IfuTvdJ9/5vZkbANjOATkbwyXlMjhSe0civtQpa9NqLShuNQWZ1UU9dlFBwH5H0YdfxuwhE2OXDCl8GZGmsgpoo0CJYPD2XKNp1mbxLym/4YzXsqQEAAA==)

### Recommended Action

Look at the ErrorCode and ErrorDetails. Consider the following actions based on the error code.
| ErrorCode | Action |
|--|--|
|RetryableError |Have customer retry the operation.|
|InUseRouteFilterCannotBeDeleted  | Look at the ErrorDetails column. It will say RouteFilter \<name> is in use by ExpressRouteBgpPeering /subscriptions/*\<subscription id>*/resourceGroups/*\<resource group name>*/providers/Microsoft.Network/expressRouteCircuits/*\<circuit name>*/peerings/MicrosoftPeering. Instruct the customer to dis-associate the route filter from that peering.|
