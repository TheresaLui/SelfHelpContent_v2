<properties
pageTitle="Gateway Service Failed To Start"
description="Gateway Service Failed To Start"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="1"
articleId="VNGTenantLogsGatewayServiceFailedToStartInsight"
diagnosticScenario="VNGTenantLogsGatewayServiceFailedToStartInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# The virtual network gateway is not started
<!--issueDescription-->
We have identified that one of your Virtual Network Gateway instances for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of: **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has not started the gateway service with a reason of: **<!--$reason-->[reason]<!--/$reason-->**. Your VPN connection could be impacted in the event the other gateway instance needs updating or you have a ['highly available VPN configuration'](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-highlyavailable).
<!--/issueDescription-->
## **Issue Summary & Mitigation**
Azure Virtual Network Gateways are deployed in a high availability set to increase uptime. Issues like this, although not common, can occur and your VPN tunnel should remain working while the other instance is 'healed'. If this event has resulted in persistent tunnel establishment failure, attempt to [reset the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). If a Reset does not provide relief, consider deleting and re-creating the Gateway.
### Steps to recreate the Virtual Network Gateway
Please Note: **REQUIRES up to 45 minutes of VPN DOWNTIME** and on-premises VPN device configuration updates.

1. Open the **[Azure portal](http://portal.azure.com)**
2. Find your Vnet Gateway for VNet: **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->**
3. Open the **Overview** blade and press the **Delete** button at the top. * **NOTE**: Your VPN connection to your Virtual Network, **<!--$vnetName-->[vnetName]<!--/$vnetName-->**, will go down at this point.
4. Finish by creating a new Virtual Network Gateway and updating your on-premises device by following steps 4-8 [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal#VNetGateway)

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation).**
