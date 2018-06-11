<properties
pageTitle="Virtual Network Gateway High Bandwidth Utilization Detected"
description="Virtual Network Gateway High Bandwidth Utilization Detected"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGVirtualNetworkGatewayHighBandwidthUtilizationInsight2"
diagnosticScenario="VNGVirtualNetworkGatewayHighBandwidthUtilizationInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Microsoft Azure has identified the Virtual Network Gateway has high bandwidth utilization
<!--issueDescription-->
We have identified that your Virtual Network Gateway for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of  **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has averaged **<!--$sumMbps-->[sumMbps]<!--/$sumMbps-->** Mbps for a duration of at least 1 minute. Maximum throughput for VNet Gateway SKU **'<!--$gatewaySku-->[gatewaySku]<!--/$gatewaySku-->'** is **<!--$maxMbps-->[maxMbps]<!--/$maxMbps-->** Mbps. The most recent time reported: **<!--$timestamp-->[timestamp]<!--/$timestamp-->**.
<!--/issueDescription-->
## **Issue Summary & Recommendations**
If your virtual network gateways become over utilized you may begin to see intermittent connection issues. We recommend scaling up to a larger SKU to match your peak bandwidth usage times. Gateway SKU throughput benchmarks can be reviewed [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings#gwsku). Instructions on resizing your gateway can be found [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings#resizechange).

We recommend enabling **Virtual Network Gateway Metrics** to monitor and detect issues like this proactively. To enable Metrics: 
1. Go to the [Azure portal](http://portal.azure.com)
2. Find your Virtual Network Gateway
3. Open the 'Metrics' blade
4. Choose the applicable metric from the drop down. (S2S Bandwidth)
5. If the issue happens again:
   1. Review VNet Gateway metrics in the 'Metrics' blade around the same time. Note the peak bandwidth around the time of the failover. 
   2. Make note of your gateways SKU from the 'Overview' blade
   3. Browse to the SKU benchmarks outlined [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku) and compare the Bandwidth metric in the 'Metrics' blade with your Virtual Network Gateway's SKU.

### For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation).
