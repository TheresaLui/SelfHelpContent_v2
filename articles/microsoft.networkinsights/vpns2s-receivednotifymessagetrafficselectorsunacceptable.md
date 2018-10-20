<properties
pageTitle="VPN tunnel disconnected due to rejected Traffic Selectors"
description="My VPN tunnel is disconnected due to rejected Traffic Selectors"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
displayOrder="10"
articleId="ReceivedNotifyMessageTrafficSelectorsUnacceptable"
diagnosticScenario="ReceivedNotifyMessageTrafficSelectorsUnacceptable"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Microsoft Azure has detected an IKE Traffic Selector policy issue on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because the on-premises VPN device rejected IKE Traffic Selectors sent from your Azure VPN gateway. Azure route-based VPN gateways by default use **any-to-any (0.0.0.0/0)** traffic selectors; or if you specify **UsePolicyBasedTrafficSelectors** option, Azure gateways will send the Traffic Selectors consist of your virtual network address prefixes and your on-premises network address prefixes.

## Recommended steps
Verify the Traffic Selectors configured on your VPN device can accept the proposals sent from your Azure VPN gateways:

1. If you have a route-based VPN device, verify the Traffic Selectors (or network address spaces) setting is either blank or 0.0.0.0/0 (wildcard/any address). Refer to the instructions of your VPN devices
2. If you have a policy-based VPN firewall, set the **UsePolicyBasedTrafficSelectors** option on the Azure VPN tunnel, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, following the steps in this [document](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-connect-multiple-policybased-rm-ps)

## Recommended documents

* [Configure policy-based VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-connect-multiple-policybased-rm-ps)
* [Create and manage S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-vpnconnection-powershell)
* [About on-premises VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#devicetable)
