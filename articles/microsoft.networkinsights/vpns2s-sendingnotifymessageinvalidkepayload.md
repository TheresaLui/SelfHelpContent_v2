<properties
pageTitle="VPN tunnel negotiation failed due to IKE Diffie-Hellman group mismatch"
description="My VPN tunnel is disconnected due to mismatch in IKE Diffie-Hellman group"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
ms.author="yushwang"
displayOrder="10"
articleId="SendingNotifyMessageInvalidKEPayload"
diagnosticScenario="SendingNotifyMessageInvalidKEPayload"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Microsoft Azure has detected an IPsec/IKE Diffie-Hellman (DH) group mismatch on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because of mismatch of the IKE Diffie-Hellman (DH) group setting between your on-premises VPN device and your Azure VPN gateway. You can ignore this warning if the VPN tunnel is connected and working, as it could recover automatically during the subsequent IKE negotiation.

## Recommended Steps

1. Verify the IPsec/IKE algorithms and parameters, specifically the Diffie-Hellman group setting, configured on your VPN device match the policies supported by the [Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)

2. If there is no matching policy that works with your VPN device, or you require a specific Diffie-Hellman group due to compliance requirements, configure a [custom policy on the connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)

## Recommended Documents

* [Supported IPsec/IKE algorithms and policies on Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
* [About cryptographic requirements](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-compliance-crypto)
* [Configure IPsec/IKE policy for VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)
