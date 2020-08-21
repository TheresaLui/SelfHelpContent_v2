<properties
pageTitle="VPN tunnel disconnected due to IKE negotiation timeout"
description="My VPN tunnel is disconnected due to IKE negotiation timeout"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
displayOrder="10"
articleId="TimedRWithErrorNegotiationNegotiationOut"
diagnosticScenario="TimedRWithErrorNegotiationNegotiationOut"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Microsoft Azure has detected connection timeout on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because the IKE negotiation timed out. The Azure VPN gateway, **<!--$VpnGatewayName-->[VpnGatewayName]<!--/$VpnGatewayName-->**, could not receive the IKE packets sent from your VPN device, or your VPN device is not responding to the Azure VPN gateway. There may be network connectivity issues between your VPN device and your Azure VPN gateway, or misconfigurations either on your VPN device or the Azure VPN connections.

## Recommended steps

Follow the instruction manual of your VPN device to check if it received any IKE packet from your Azure VPN gateway:

1. If there is no packet received from your Azure VPN gateway:

   * Verify if there is [network connectivity issues](https://azure.microsoft.com/status/) between your on-premises network and the Azure region of your gateway
   * Check if the [local network gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-modify-local-network-gateway-portal) resource representing your on-premises network contains the correct public IP address of your VPN device
   * Check if your Azure VPN gateway is working correctly by navigating to the "Resource health" page of your Azure VPN gateway on the [Azure Portal](https://portal.azure.com)

2. If the packets from your Azure VPN gateway were detected:

   * Refer to your VPN device manual to verify your device IPsec/IKE policy is configured correctly for this VPN connection
   * Verify your [Azure VPN connection parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) can work with your IPsec/IKE configuration
   * If necessary, specify a [custom IPsec/IKE policy](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) that meet your on-premises VPN device settings

## Recommended documents

* [About on-premises VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#devicetable)
* [Manage your local network gateway settings](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-modify-local-network-gateway-portal)
* [IPsec/IKE parameters on Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
* [Configure IPsec/IKE policy for VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) 
* [Create and manage S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-vpnconnection-powershell)
