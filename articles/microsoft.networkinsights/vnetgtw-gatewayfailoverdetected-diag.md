<properties
pageTitle="My Virtual Network Gateway Failover Detected"
description="My Virtual Network Gateway Failover Detected"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGTenantEventsGatewayFailoverDetectedSecondaryInsight"
diagnosticScenario="VNGTenantEventsGatewayFailoverDetectedSecondaryInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Virtual network gateway has switched over to a backup instance
<!--issueDescription-->
We have identified that your Virtual Network Gateway for Vnet **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of: **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has switched over to another instance. The most recent time reported: **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**. This behavior can be considered normal and typically occurs during planned maintenance of the VNet Gateway and should not impact active VPN workloads using active-passive gateway deployments. You are affected by this if you are using an active-active VPN deployment. If configured properly your VPN connection to your Vnet will remain but you may have noticed some sessions disconnected at the above time. You were also without VPN Tunnel redundancy during this time.
<!--/issueDescription-->
## **Details & Mitigation**
 If this failover event resulted in persistent tunnel establishment failure, consider [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic).  

We recommend enabling **Virtual Network Gateway Metrics** to monitor your VPN Gateways pro-actively.

1. Go to the [Azure portal](http://portal.azure.com)
2. Find your Virtual Network Gateway
3. Open the 'Metrics' blade
4. Choose the applicable metric from the drop down. (S2S Bandwidth)
5. If the issue happens again:
   1. Review VNet Gateway metrics in the 'Metrics' blade around the same time. Note the peak bandwidth around the time of the failover. 
   2. Make note of your gateways SKU from the 'Overview' blade
   3. Browse to the SKU benchmarks outlined [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku) and compare the Bandwidth metric in the 'Metrics' blade with your Virtual Network Gateway's SKU.

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation).**

Microsoft is continuously working to identify and resolve issues proactively. Please feel free to reach out with any questions in the meantime.
