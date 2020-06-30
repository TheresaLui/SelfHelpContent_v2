<properties
pageTitle="VPN tunnel disconnected due to a VPN platform failure"
description="My VPN tunnel is disconnected due to an internal failure on the Azure VPN gateway"
infoBubbleText="Issues with your VPN gateway or S2S VPN connection were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="yushwang"
displayOrder="10"
articleId="ReceivedNotifywitherrorTheReadOrWriteOperationToAnEncryptedFileCouldNotBeCompleted"
diagnosticScenario="ReceivedNotifywitherrorTheReadOrWriteOperationToAnEncryptedFileCouldNotBeCompleted"
selfHelpType="Diagnostics"
supportTopicIds="32591144,32591145,32591158"
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Microsoft Azure has detected an internal platform issue with your VPN gateway
<!--issueDescription-->
We have identified that your VPN connection, **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->**, is disconnected because the VPN gateway, **<!--$VpnGatewayName-->[VpnGatewayName]<!--/$VpnGatewayName-->**, has encountered an internal platform issue. This is usually a temporary condition, the gateway and the connection should auto-recover shortly.

## Recommended steps

1. Check if your VPN connection is working correctly. You can also check the Resource health of your gateway and connection. From the [Azure Portal](https://portal.azure.com), navigate to your VPN gateway or your connection resource, and click "Resource health". Resource health page contains the current status, and the health history for the last 2 weeks.

2. If the VPN connection is still broken, you can reset the VPN gateway by clicking the "Reset" link on your VPN gateway page in the portal.

## Recommended documents

* [Reset a VPN gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic)
* [Troubleshoot VPN gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot)
* [Troubleshoot VPN connectivity with Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-troubleshoot-overview)
