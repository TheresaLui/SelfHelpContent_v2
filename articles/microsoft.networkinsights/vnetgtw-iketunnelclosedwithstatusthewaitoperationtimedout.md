<properties
pageTitle="My Virtual Network Gateway VPN Tunnel is Disconnected"
description="My Virtual Network Gateway VPN Tunnel is Disconnected"
infoBubbleText="Your VPN Tunnel Could Not Connect. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="IkeTunnelClosedWithStatusTheWaitOperationTimedout"
diagnosticScenario="IkeTunnelClosedWithStatusTheWaitOperationTimedout"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# VPN Tunnel Connection Timed Out
<!--issueDescription-->
We have identified that tunnel **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->** could not connect due to a timeout at **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**.
## **Mitigation Steps**
If the tunnel reconnects in a few minutes then no action is necessary, otherwise try [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic).

