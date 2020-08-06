<properties
pageTitle="My Virtual Network Gateway is missing peering with the Microsoft Edge Router"
description="My Virtual Network Gateway is missing peering with the Microsoft Edge Router"
infoBubbleText="Issues with your Vnet Gateway Peering were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGTenantEventsExpressRouteMissingPeeringInsight2"
diagnosticScenario="VNGTenantEventsExpressRouteMissingPeeringInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Peering is missing between the VNet Gateway and the Microsoft Edge Router (MSEE)
<!--issueDescription-->
We have identified an Azure platform configuration issue. Your Virtual Network Gateway for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of: **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has no peering established to the Microsoft Edge Router (MSEE) with a peer IP of: **<!--$peerip-->[peerip]<!--/$peerip-->**. The most recent time reported is: **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**.
<!--/issueDescription-->

## **Issue Details & Mitigation**
We have identified a platform configuration issue and are working with the appropriate teams to mitigate this issue as quickly as possible and return you to normal operations. If you would prefer to forfeit a detailed root cause analysis and expedite the resolution of connectivity consider removing and re-creating the ExpressRoute Connection in the [Azure portal](http://portal.azure.com) and [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). 

Microsoft is continuously working to identify and resolve issues proactively.  We will contact you as soon as the issue is mitigated to ensure you're no longer impacted.  Please feel free to reach out with any questions in the meantime.  Again, we apologize for the inconvenience. 

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation)**.
