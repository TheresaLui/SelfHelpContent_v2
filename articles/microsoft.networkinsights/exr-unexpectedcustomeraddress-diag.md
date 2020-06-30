<properties
pageTitle="My ExpressRoute has an unexpected IP address in use."
description="My ExpressRoute has an unexpected IP address in use."
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="chadmat"
displayOrder="10"
articleId="ExRVNetGatewayUnexpectedBgpPeerCaIpAddressInsight"
diagnosticScenario="ExRVNetGatewayUnexpectedBgpPeerCaIpAddressInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute BGP Peer Has Unexpected IP Address
<!--issueDescription-->
We have identified a platform configuration issue for your private peering ExpressRoute connection that uses ServiceKey: **<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**. The initial diagnosis is showing that the virtual network gateway, which is a BGP peer of the Microsoft Edge router, has an unexpected IP address. See below for steps to resolve the issue.
<!--/issueDescription-->
## **Steps to resolve this issue**
**Note:** VNet Gateways **MUST** use the default Vnet IPs assigned on the gateway subnet. The following steps will resolve the issue by decommissioning the current VPN gateways and provisioning new VPN gateways with the appropriate IP address.

1. Remove the VNet circuit link (connection)
2. Delete the ExpressRoute VNet gateway
3. Wait approximately 15 minutes to ensure platform clean up tasks complete
4. Recreate the ExpressRoute VNet gateway
5. Finally recreate the circuit link (connection).
<br>
Microsoft is continuously working to identify and resolve issues proactively. Please feel free to reach out with any questions. Again, we apologize for the inconvenience. 
