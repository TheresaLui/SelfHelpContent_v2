<properties
pageTitle="My Virtual Network Gateway Failover Detected"
description="My Virtual Network Gateway Failover Detected"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="anzaman"
displayOrder="10"
articleId="VNGVirtualNetworkGatewayResetDetectedInsight"
diagnosticScenario="VNGVirtualNetworkGatewayResetDetectedInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Virtual network gateway was reset
<!--issueDescription-->
We have identified your Virtual Network Gateway in Azure Subscription: {customerSubscriptionId} was recently reset around {preciseTimeStamp}. This is a user initiated operation. The VPN connection to your VNet will remain but you may have noticed some sessions disconnected at the above time. Also, the VPN Tunnel was not redundant during this time.
<!--/issueDescription-->
## **Mitigation Steps**
 If this reset resulted in persistent tunnel establishment failure, consider [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic) again as a second reset will reboot the second instance of the gateway.

