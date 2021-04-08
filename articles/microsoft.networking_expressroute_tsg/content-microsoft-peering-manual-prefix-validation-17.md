# Microsoft Peering Manual Prefix validation

<properties
pageTitle="Microsoft Peering Manual Prefix validation"
description="Microsoft Peering Manual Prefix validation"
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
articleId="14a19f3e-4937-4a4e-8891-f5edcf09d38e"
ownershipId="CloudNet_AzureExpressRoute"
/>

## Validating prefix for Microsoft Peering

### Recommended Action

* On Microsoft Peering, we expect customer to advertise Public IP ranges which is owned by them over the Microsoft peering. But some time while configuring the Microsoft peering or updating the peering with additional customer prefixes, customer would see "Validation needed".
* To confirm the issue from ASC, navigate to ExpressRoute circuit > Properties > DumpCircuitInfo. You can also collect it from Jarvis Actions.
* Under "Microsoft Peering" check the section "*VALIDATION NEEDED ADVERTISED PREFIXES: \<Customer Owned Public IP Address\>*" to see the list of customer IP address needs manual validation.
* Refer our [internal ANP Wiki link](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/137958/How-to-Manually-Validate-ASN-and-Public-Prefixes-for-ExR) to learn more

### Solution

To fix this issue, reach out to your TA with Letter of Authorization (LoA) from customer for manual validation.
