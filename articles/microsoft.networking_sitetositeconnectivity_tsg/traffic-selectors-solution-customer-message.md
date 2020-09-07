<properties
pageTitle="Traffic selectors are leading to connectivity issues"
description="Traffic selectors are leading to connectivity issues"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="5d0342a7-0098-4fe1-a5e4-3b485419a5dc"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# Traffic selectors are leading to connectivity issues

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We're reviewed the logs and diagnostics available to us and have determined that your connectivity is the result of narrow traffic selectors. Traffic selectors are a VPN configuration that only allows certain subnets to talk to other subnets. Traffic selectors can be configured on either the Azure VPN Gateway or on the on-premise VPN device. In order to resolve your connectivity issues, the traffic selectors must be configured to allow the subnets that require connectivity. Additionally, traffic selector configuration must match on both sides of the VPN connection.

Best regards,
<!--/issueDescription-->