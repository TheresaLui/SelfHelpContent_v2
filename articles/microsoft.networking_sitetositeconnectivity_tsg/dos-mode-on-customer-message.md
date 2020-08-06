<properties
pageTitle="Repeated connection attempts from on-premise device leading to DoS Protection"
description="Repeated connection attempts from on-premise device leading to DoS Protection"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="aab84c2c-18f5-4c7d-b8e0-e77fbb8030f1"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# Repeated connection attempts from on-premise device leading to DoS Protection

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your VPN Gateway connectivity issue. We've looking into our diagnostic logs and have determined that the connectivity issue is due to the Azure VPN Gateway being in "DoS Protection Mode". This situation occurs when VPN Gateway has more than 500 outstanding/incomplete security associations. This typically is a result of an unhealthy on-premise VPN device. The first step in resolving this connectivity issue is ensuring the on-premise device is healthy (typically by rebooting it) and then resetting the Azure VPN Gateway to clear the DoS Protection Mode. Please take necessary steps to bring your on-premise device to a healthy state and let us know when complete.

Best Regards,
<!--/issueDescription-->