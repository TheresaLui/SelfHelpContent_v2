<properties
pageTitle="My Virtual Network Gateway VPN Tunnel is Disconnected"
description="My Virtual Network Gateway VPN Tunnel is Disconnected"
infoBubbleText="Your VPN Tunnel Could Not Connect. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="anzaman"
displayOrder="10"
articleId="IkeTunnelClosedWithStatusTheOperatororAdministratorHasRefusedTheRequest"
diagnosticScenario="IkeTunnelClosedWithStatusTheOperatororAdministratorHasRefusedTheRequest"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# VPN Tunnel Connection Was Disconnected
<!--issueDescription-->
We have identified that tunnel {TunnelId} was disconnected because the Gateway received a connect request on an alreading connecting/connected state tunnel or the Connection request was received on a Secondary gateway instance.<!--/$preciseTimestamp-->**.
## **Issue Details & Mitigation**
If the tunnel reconnects in a few minutes then no action is necessary, otherwise try [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic).

