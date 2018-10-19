<properties
pageTitle="My Virtual Network Gateway VPN Tunnel Changed to Disconnected"
description="My Virtual Network Gateway VPN Tunnel Changed to Disconnected"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="10"
articleId="IkeTunnelClosedWithStatusTheUsernameOrPasswordIsIncorrect"
diagnosticScenario="IkeTunnelClosedWithStatusTheUsernameOrPasswordIsIncorrect"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Incorrect Username or Password
<!--issueDescription-->
We have identified that tunnel **<!--$TunnelName-->[TunnelName]<!--/$TunnelName-->** could not connect due to incorrect credentials at **<!--$preciseTimestamp-->[preciseTimestamp]<!--/$preciseTimestamp-->**.
## **Issue Details & Mitigation**
If using login id and password, please check your credentials and try to connect again. 

If using certificates, make sure that the correct certificate is installed and used.

Make sure that the user is authorized to connect via VPN if using RADIUS.

