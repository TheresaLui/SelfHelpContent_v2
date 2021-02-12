<properties
pageTitle="Message with invalid syntax"
description="Message with invalid syntax received"
infoBubbleText="Issues with your VirtualNetworkGateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="anzaman"
displayOrder="10"
articleId="ReceivedNotifyMessageInvalidSyntax"
diagnosticScenario="ReceivedNotifyMessageInvalidSyntax"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# The gateway received a Notify Message with an invalid syntax
<!--issueDescription-->
We have identified that the VPN tunnel was disconnected because the gateway {VpnGatewayName} received a Notify Message with an invalid syntax.
<!--/issueDescription-->
## **Issue Details & Mitigation**
We have identified that the VPN tunnel was disconnected because the Azure VPN gateway received a Notify Message from your on-premises device that had an invalid syntax. Please check your on-premises device and suppress invalid Notify Messages.

We recommend enabling **Virtual Network Gateway Metrics** to monitor and detect issues proactively. To enable Metrics: 

1. Go to the [Azure portal](http://portal.azure.com)
2. Find your Virtual Network Gateway
3. Open the 'Metrics' blade
4. Choose the applicable metric from the drop down.
5. If the issue happens again:
   1. Review VNet Gateway metrics in the 'Metrics' blade around the same time. Note the peak bandwidth around the time of the failover. 
   2. Make note of your gateway's SKU from the 'Overview' blade
   3. Browse to the SKU benchmarks outlined [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku) and compare the Bandwidth metric in the 'Metrics' blade with your Virtual Network Gateway's SKU.

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. 
More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation)**.
