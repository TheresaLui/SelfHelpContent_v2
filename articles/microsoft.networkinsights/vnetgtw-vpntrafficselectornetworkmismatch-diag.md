<properties
pageTitle="VPN tunnel disconnected due to IPsec/IKE traffic selectors mismatch"
description="My VPN tunnel is disconnected due to mismatch in IPsec/IKE traffic selectors"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang, seanj-ms"
ms.author="yushwang, seanj"
displayOrder="10"
articleId="VPNGatewayTrafficSelectorMismatchInsight"
diagnosticScenario="VpnGwyTrafficSelector"
selfHelpType="Diagnostics"
supportTopicIds="32591144, 32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds="16094"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Microsoft Azure has detected an IPsec/IKE traffic selectors mismatch on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection is disconnected because your on-premises VPN device rejected the traffic selectors proposed by your Azure VPN gateway. Azure VPN gateways by default use wildcard (any-to-any) traffic selectors in a route-based configuration; or you can enable ["UsePolicyBasedTrafficSelectors"](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-connect-multiple-policybased-rm-ps) option on your VPN connection, where Azure gateways will use the combinations of your virtual network prefixes and your [on-premises network prefixes](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-modify-local-network-gateway-portal) as the traffic selectors.

## Recommended Steps

1. Verify if the traffic selectors configured on [your VPN device](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#devicetable) accept the wildcard (any-to-any) traffic selectors proposed by your Azure VPN gateway. Some VPN devices use "access lists" to define traffic selectors.

The currently selected **<!--$defaultText-->[defaultText]<!--/$defaultText-->** traffic selector range **<!--$startingIpAddress-->[startingIpAddress]<!--/$startingIpAddress-->** - **<!--$endingIpAddress-->[endingIpAddress]<!--/$endingIpAddress-->** does not match any local gateway subnets.

2. If your VPN device does **not** accept wildcard (any-to-any) traffic selectors, enable the ["UsePolicyBasedTrafficSelectors"](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-connect-multiple-policybased-rm-ps) option on your VPN connection, and configure traffic selectors on your device with the combinations of your [on-premises network prefixes](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-modify-local-network-gateway-portal) to your Azure virtual network address range.

## Recommended Documents

* [Create and manage S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-vpnconnection-powershell)
