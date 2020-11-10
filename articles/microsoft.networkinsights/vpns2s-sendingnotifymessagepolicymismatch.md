<properties
pageTitle="VPN tunnel disconnected due to IPsec/IKE policy mismatch"
description="My VPN tunnel is disconnected due to mismatch in IPsec/IKE cryptographic algorithms or policies"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
displayOrder="10"
articleId="SendingNotifyMessagePolicyMismatch"
diagnosticScenario="SendingNotifyMessagePolicyMismatch"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Microsoft Azure has detected an IPsec/IKE policy mismatch on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because of mismatch of the IPsec/IKE cryptographic algorithms and policies between your on-premises VPN device and your Azure VPN gateway. This could also happen in a VNet-to-VNet connection using Azure VPN gateways if the configurations are not the same for the two connection resources.

## Recommended steps

1. Verify the IPsec/IKE algorithms and parameters configured on your VPN device match the policies supported by the Azure VPN gateways as listed [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)

2. If there is no matching policy that works with your VPN device, or you need a specific algorithm or key strength due to compliance requirements, configure a custom policy on the connection as described in this [document](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)

## Recommended documents

* [Supported IPsec/IKE algorithms and policies on Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
* [About cryptographic requirements](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-compliance-crypto)
* [Configure IPsec/IKE policy for VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)