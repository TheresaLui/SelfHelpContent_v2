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
cloudEnvironments="Public"
/>
# Microsoft Azure has detected timeout on your VPN connection
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because the on-premises VPN device is not responding to the Azure VPN gateway. This could happen due to network connectivity issue between your VPN device and your Azure VPN gateway, or misconfigurations either on your VPN device or the Azure VPN connections.

## Recommended steps

1. Check your VPN device log to see if the IKE packets from your Azure VPN gateway had reached your VPN device. Refer to your VPN device instruction manual
2. If the packets from Azure VPN gateway were detected, verify your device configuration to see if the IPsec/IKE policy is configured correctly for the VPN connection
3. If the packets were not detected on your VPN device, 

1. 
2.  Reset the Azure VPN gateway. From the [Azure Portal](https://portal.azure.com), navigate to your VPN gateway. Click the "Reset" link and follow the instructions
3. Verify and change your SA lifetime on the Azure connection or your VPN device to different values to prevent this from happening again
    * The default Azure VPN SA lifetimes are listed [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
    * Follow the [instructions](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) to set a different SA lifetime value on your VPN connection
    * Refer to your VPN device instruction manual to check the SA lifetime values

## Recommended documents

* [IPsec/IKE parameters on Azure VPN gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec)
* [Configure IPsec/IKE policy for VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) 
* [Create and manage S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-tutorial-vpnconnection-powershell)
* [About on-premises VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#devicetable)
