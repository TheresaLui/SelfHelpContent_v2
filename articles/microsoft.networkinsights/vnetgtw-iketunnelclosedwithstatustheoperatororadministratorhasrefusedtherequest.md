<properties
pageTitle="My Virtual Network Gateway VPN Tunnel is Disconnected"
description="My Virtual Network Gateway VPN Tunnel is Disconnected"
infoBubbleText="Your VPN Tunnel Could Not Connect. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="IkeTunnelClosedWithStatusTheOperatororAdministratorHasRefusedTheRequest"
diagnosticScenario="IkeTunnelClosedWithStatusTheOperatororAdministratorHasRefusedTheRequest"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# VPN Tunnel Connection Was Disconnected
<!--issueDescription-->
We have identified that tunnel {TunnelId} was disconnected because the Gateway received a connection request on a tunnel that is already in connecting/connected state or the connection request was received on a secondary gateway instance. 
## **Mitigation Steps**
If the tunnel reconnects in a few minutes then no action is necessary, otherwise try [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic).

