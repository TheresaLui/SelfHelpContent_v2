<properties
pageTitle="On-premise VPN device is behaving in an supported way"
description="On-premise VPN device is behaving in an supported way"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="d1f355e8-00e9-4c3d-85c5-dcf3b1bf8dda"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# On-premise VPN device is behaving in an supported way

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We've reviewed the logs and diagnostics available to us and have determined that your on-premise VPN device is attempting to change the connection parameters after an IPSec tunnel is already established. This is not a supported capability of Azure VPN Gateway. Often times, this is caused by the on-premise device missing the "lifetime in bytes" configuration. Please correct your on-premise device or work with your on-premise device vendor to ensure it does not attempt to change connection parameters after an IPSec session is established.

Best regards,
<!--/issueDescription-->