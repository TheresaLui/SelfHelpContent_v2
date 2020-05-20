<properties
pageTitle="My Virtual Network Gateway is missing customer on-premises routes"
description="My Virtual Network Gateway is missing customer on-premises routes"
infoBubbleText="Issues with your Vnet Gateway Peering were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGTenantEventsExpressRouteLinkNoCustomerRoutesFoundInsight2"
diagnosticScenario="VNGTenantEventsExpressRouteLinkNoCustomerRoutesFoundInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# ExpressRoute routes are missing on the VNet Gateway
<!--issueDescription-->
We have identified an Azure platform configuration issue. Your Virtual Network Gateway for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of  **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has not learned the on-premises routes from the ExpressRoute Circuit Link. The most recent time reported is: **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**.
<!--/issueDescription-->
## **Issue Details & Mitigation**
We have identified a potential configuration issue and are working with the appropriate teams to mitigate this issue as quickly as possible and return you to normal operations. If you would prefer to forfeit a detailed root cause analysis and expedite the resolution of connectivity consider removing and recreating the ExpressRoute Connection in the [Azure portal](http://portal.azure.com) and [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). 

Microsoft is continuously working to identify and resolve issues proactively.  We will contact you as soon as the issue is mitigated to ensure you're no longer impacted.  Please feel free to reach out with any questions in the meantime.  Again, we apologize for the inconvenience. 

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation).**
