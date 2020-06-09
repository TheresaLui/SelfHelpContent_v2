<properties
pageTitle="Customer device may be unsupported or configured as a Responder only"
description="Customer device may be unsupported or configured as a Responder only"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="fb7dea42-33de-4473-bc12-4d05d92746e7"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# Customer device may be unsupported or configured as a Responder only

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We’ve reviewed the logs and diagnostics available to us and have determined that no IKE negotiation packets are being seen on the Azure VPN Gateway. This may be because your on-premise VPN device is configured as a "Responder" and not an "Initiator". We recommend configuring on-premise device both as Responder and Initiator. If this is not possible, then please generate traffic from Azure towards your on-premise network in order to bring up the VPN connection.  

Best regards,
<!--/issueDescription-->
