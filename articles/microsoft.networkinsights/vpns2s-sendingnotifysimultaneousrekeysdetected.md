<properties
pageTitle="VPN tunnel disconnected due to simultaneous rekeying"
description="My VPN tunnel is disconnected due to simultaneous rekeying"
infoBubbleText="Issues with your S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
displayOrder="10"
articleId="SendingNotifywitherrorSimultaneousRekeysWereDetected"
diagnosticScenario="SendingNotifywitherrorSimultaneousRekeysWereDetected"
selfHelpType="Diagnostics"
supportTopicIds="32591145,32591158,32591149,32591152,32591155"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Microsoft Azure has detected your S2S tunnel disconnected due to simultaneous rekeying

<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because the tunnel state (IKE SA or Security Association) is either timed out or deleted. This could happen when the on-premises VPN device and your Azure VPN gateway are trying to rekey at the same time, resulting in a short interruption of your VPN connection.

## Recommended steps

The connection should recover shortly. If the connectivity is not restored, you can take the following actions:

1. Reset the Azure VPN gateway. From the [Azure Portal](https://portal.azure.com), navigate to your VPN gateway, **<!--$VpnGatewayName-->[VpnGatewayName]<!--/$VpnGatewayName-->**. Click the "Reset" link and follow the instructions
2. Verify and change your SA lifetime for the Azure connection or your VPN device to different values to prevent this from happening again
    * The recommendation is to set the SA lifetime on your VPN devices to be **longer** than the values used by the Azure VPN gateways
    * The default Azure VPN SA lifetimes are listed [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
    * Follow the [instructions](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) to set a different SA lifetime value on your VPN connection
    * Refer to your VPN device instruction manual to check the SA lifetime values

## Recommended documents

* [IPsec/IKE parameters on Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
* [Configure IPsec/IKE policy for VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) 
* [Create and manage S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-vpnconnection-powershell)
* [About on-premises VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#devicetable)
