<properties
pageTitle="My Virtual Network Gateway VPN Tunnel Changed to Disconnected After Planned Maintenance"
description="My Virtual Network Gateway VPN Tunnel Changed to Disconnected After Planned Maintenance"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="VNGTenantLogsGatewayFailoverDuringPlannedMaintenanceInsight"
diagnosticScenario="VNGTenantLogsGatewayFailoverDuringPlannedMaintenanceInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# The Virtual Network Gateway is disconnected
<!--issueDescription-->
We have identified that your Virtual Network Gateway for VNet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with a VIP of  **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** failed over to the passive instance due to a planned maintenance around {preciseTimeStamp}.
## **Issue Details**
During the planned maintenance, the VPN connection to your Vnet will persist but you may have noticed some sessions disconnected at the above time. You were also without VPN Tunnel [redundancy](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-highlyavailable) during this time.


