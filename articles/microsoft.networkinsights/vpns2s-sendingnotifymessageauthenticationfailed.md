<properties
pageTitle="VPN tunnel disconnected due to pre-shared key mismatch"
description="My VPN tunnel is disconnected due to pre-shared key mismatch"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
displayOrder="10"
articleId="SendingNotifyMessageAuthenticationFailed"
diagnosticScenario="SendingNotifyMessageAuthenticationFailed"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Microsoft Azure has detected a pre-shared key mismatch on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because of mismatch of the pre-shared keys configured on your on-premises VPN device and your Azure VPN gateway. This could also happen in a VNet-to-VNet connection using Azure VPN gateways if the pre-shared keys are not the same for the two connection resources.

## Recommended steps
Verify the pre-shared key for the VPN connection matches what you have configured on your VPN device:

1. Go to the [Azure portal](http://portal.azure.com)
2. Find your VPN connection: **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**
3. Open the "Shared key" page of the VPN connection
4. Verify and update the pre-shared key if necessary. The pre-shared key must be a string of printable ASCII characters of length between 1 and 128 characters
5. Consult your on-premises VPN device configuration instructions to check and update the pre-shared key for this connection if needed
6. If this is a VNet-to-VNet connection, verify the pre-shared key against the matching connection from the target VNet to this VNet

## Recommended documents

* [Create and manage S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-vpnconnection-powershell)
* [Create and manage VNet-to-VNet connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager-portal)
* [About on-premises VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#devicetable)
