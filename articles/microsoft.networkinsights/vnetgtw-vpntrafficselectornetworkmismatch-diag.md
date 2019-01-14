<properties
pageTitle="VPN Gateway Traffic Selector Network Mismatch"
description=" VPN Gateway Traffic Selector Network Mismatch "
infoBubbleText=" VPN Gateway Traffic Selector Network Mismatch. See details on the right."
service="microsoft.network"
resource="virtualNetworkGateways"
authors="seanj"
displayOrder=""
articleId="VPNGatewayTrafficSelectorMismatchInsight"
selfHelpType="Diagnostics"
supportTopicIds="32591144, 32591149, 32591145, 32591158"
resourceTags="windows"
productPesIds="16094"
cloudEnvironments="Public"
/>
# VPN Gateway Traffic Selector Network Mismatch
<!--issueDescription-->
The traffic selector range **<!--$startingIpAddress-->[startingIpAddress]<!--/$startingIpAddress-->** - **<!--$endingIpAddress-->[endingIpAddress]<!--/$endingIpAddress-->** does not match any local gateway subnets. This may prevent successful connectivity to resources through the VPN tunnel. See below for steps to resolve the issue.
<!--/issueDescription-->
## **Steps to resolve this issue**
**Note:** The following steps will resolve the issue by examining the IP configuration of the traffic selector and of all local network gateways.

1. Review the subnet range for the traffic selector and the subnet ranges of all local network gateways. The traffic selector’s subnet should be within the subnet range of one local network gateway.
2. If the traffic selector’s subnet range does not fall within the subnet range of a local network gateway, modify it to map to the desired subnet.
3. Confirm that the current ports and protocol Id values (**<!--$defaultText-->[defaultText]<!--/$defaultText-->**) are appropriate. The default values are (port start: 0 port end: 65535 protocol id: 0) and should allow all protocols on all ports. An incorrect non-default value could cause communication problems.
