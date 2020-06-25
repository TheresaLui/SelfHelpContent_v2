<properties
pageTitle="Connection reset due to dead peer detection failures"
description="Connection reset due to dead peer detection failures"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="2df9d5e5-32b3-4af2-a018-d046b94f5f0b"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# Connection reset due to dead peer detection failures

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your VPN Gateway issue. We've looked at the diagnostic information we have available and have determined that the connectivity issue was due to your on-premise VPN device not responding to Azure VPN Gateway Dead-Peer-Detection requests. These requests are meant to ensure the remote, on-premise VPN device is available and can maintain an active tunnel. Our diagnostic logs indicate your on-premise device stopped responding to Dead-Peer-Detection (DPD) requests. The next step in troubleshooting is to determine if you have logs from your on-premise device showing it was correctly responding to DPD requests. This will help us further diagnose the root cause of this issue.

Best Regards,
<!--/issueDescription-->