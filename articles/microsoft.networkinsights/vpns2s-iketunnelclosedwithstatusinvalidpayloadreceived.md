<properties
pageTitle="VPN tunnel disconnected due to invalid IKE payload"
description="My VPN tunnel is disconnected due to IKE errors"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
ms.author="yushwang"
displayOrder="10"
articleId="IkeTunnelClosedWithStatusInvalidPayloadReceived"
diagnosticScenario="IkeTunnelClosedWithStatusInvalidPayloadReceived"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Microsoft Azure has detected an IPsec/IKE issue on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because your Azure VPN gateway received invalid payload from your on-premises VPN device. You can ignore this warning if the VPN tunnel is connected and working right now, as it could recover automatically during the subsequent IKE negotiation.

## Recommended Steps

1. Verify the IPsec/IKE algorithms and parameters configured on your VPN device match the policies [supported by the Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)

2. If there is no matching policy that works with your VPN device, or you need a specific algorithm or key strength due to compliance requirements, [configure a custom policy on the connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)

3. If the connectivity issue persists, consult the instruction manual of your VPN device to check the logs for more detailed information

## Recommended Documents

* [Supported IPsec/IKE algorithms and policies on Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
* [About cryptographic requirements](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-compliance-crypto)
* [Configure IPsec/IKE policy for VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)
