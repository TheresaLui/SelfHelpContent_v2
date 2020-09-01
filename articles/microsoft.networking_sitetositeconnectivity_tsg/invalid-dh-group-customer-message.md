<properties
pageTitle="On-premise device using unsupported IPSec policy"
description="On-premise device using unsupported IPSec policy"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="8fd65e06-da41-479a-9301-7dab3f42dc5b"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# On-premise device using unsupported IPSec policy

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We've reviewed the logs and diagnostics available to us and have determined that the connectivity issue is due to your on-premise device using an incompatible DH group. With default settings, Azure VPN Gateways only support DH Group 2. It is possible to configure custom IPSec policies, however, we recommend configuring your on-premise device to match the Azure VPN Gateway IPSec policies.

Best regards,
<!--/issueDescription-->