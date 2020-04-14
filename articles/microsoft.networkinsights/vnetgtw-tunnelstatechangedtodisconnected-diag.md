<properties
pageTitle="My Virtual Network Gateway VPN Tunnel Changed to Disconnected"
description="My Virtual Network Gateway VPN Tunnel Changed to Disconnected"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGTenantEventsVPNTunnelStateChangedToDisconnectedInsight"
diagnosticScenario="VNGTenantEventsVPNTunnelStateChangedToDisconnectedInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# The Virtual Network Gateway is disconnected
<!--issueDescription-->
We have identified that your Virtual Network Gateway for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of  **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** connecting to **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->** transitioned from a 'Connected' state to a 'Disconnected' state at **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**.
## **Issue Details & Mitigation**
We are reviewing the current connection state to verify the issue is still occurring. If you would prefer to forfeit a detailed root cause analysis and expedite the resolution of connectiviy consider removing and re-creating the VPN Connection in the [Azure portal](http://portal.azure.com) and [resetting the gateway/s](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). 

We recommend enabling **Virtual Network Gateway Metrics** to monitor and detect issues like this proactively. To enable Metrics: 

1. Go to the [Azure portal](http://portal.azure.com)
2. Find your Virtual Network Gateway
3. Open the 'Metrics' blade
4. Choose the applicable metric from the drop down. (S2S Bandwidth)
5. If the issue happens again:
   1. Review VNet Gateway metrics in the 'Metrics' blade around the same time. Note the peak bandwidth around the time of the failover. 
   2. Make note of your gateways SKU from the 'Overview' blade
   3. Browse to the SKU benchmarks outlined [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku) and compare the Bandwidth metric in the 'Metrics' blade with your Virtual Network Gateway's SKU.

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation)**.

Microsoft is continuously working to identify and resolve issues proactively.  We will contact you as soon as the issue is mitigated to ensure you're no longer impacted.  Please feel free to reach out with any questions in the meantime.  Again, we apologize for the inconvenience. 
