<properties
pageTitle="VNet Gateway Set Configuration Call Failed"
description="VNet Gateway SetConfiguration Call Failed"
infoBubbleText="Issues with your VNet were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="1"
articleId="VNGTenantEventsGatewayConfigurationFailedInsight"
diagnosticScenario="VNGTenantEventsGatewayConfigurationFailedInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# A platform configuration issue has been detected
<!--issueDescription-->
We have identified an internal platform configuration issue affecting the Virtual Network Gateway for VNet **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of: **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** at **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**.
<!--/issueDescription-->

## **Issue Details & Mitigation**
We have identified an internal configuration error and are working with the appropriate teams to mitigate this issue as quickly as possible and return you to normal operations. If your gateway is currently in a failed state, we recommend [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). Microsoft is continuously working to identify and resolve issues proactively.  We will contact you as soon as the issue is mitigated to ensure you're no longer impacted.  Please feel free to reach out with any questions in the meantime.  Again, we apologize for the inconvenience. 

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation)**.
