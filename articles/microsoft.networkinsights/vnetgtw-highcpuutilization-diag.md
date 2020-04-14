<properties
pageTitle="Virtual Network Gateway High CPU Utilization"
description="Virtual Network Gateway High CPU Utilization"
infoBubbleText="Issues with your VirtualNetworkGateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGVirtualNetworkGatewayHighCPUUtilizationInsight"
diagnosticScenario="VNGVirtualNetworkGatewayHighCPUUtilizationInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# The virtual network gateway has high CPU utilization
<!--issueDescription-->
We have identified that one of your Virtual Network Gateway instances for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of: **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has experienced an average CPU utilization value of **<!--$avgCounterValue-->[avgCounterValue]<!--/$avgCounterValue-->**% for a period of at least 5 minutes. The most recent time reported: **<!--$timestamp-->[timestamp]<!--/$timestamp-->**.
<!--/issueDescription-->
## **Issue Details & Mitigation**
If your virtual network gateways become over utilized you may begin to see intermittent connection issues. If this occurs we recommend scaling up to a larger SKU to match your peak bandwidth usage times. Gateway SKU throughput benchmarks can be reviewed [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings#gwsku). Instructions on resizing your gateway can be found [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings#resizechange).
We recommend enabling **Virtual Network Gateway Metrics** to monitor and detect issues like this proactively. To enable Metrics: 

1. Go to the [Azure portal](http://portal.azure.com)
2. Find your Virtual Network Gateway
3. Open the 'Metrics' blade
4. Choose the applicable metric from the drop down.
5. If the issue happens again:
   1. Review VNet Gateway metrics in the 'Metrics' blade around the same time. Note the peak bandwidth around the time of the failover. 
   2. Make note of your gateways SKU from the 'Overview' blade
   3. Browse to the SKU benchmarks outlined [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku) and compare the Bandwidth metric in the 'Metrics' blade with your Virtual Network Gateway's SKU.
**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation)**.
