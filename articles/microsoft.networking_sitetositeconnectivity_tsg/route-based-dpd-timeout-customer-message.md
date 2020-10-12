<properties
pageTitle="VPN connection failed due to no response to dead peer detection pings"
description="VPN connection failed due to no response to dead peer detection pings"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="a1e00637-f650-4e11-b6c4-72d28a6e81d8"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# VPN connection failed due to no response to dead peer detection pings

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your VPN Gateway issue. We've looked at the diagnostic information we have available and have determined that the connectivity issue was due to your on-premise VPN device not responding to Azure VPN Gateway Dead-Peer-Detection requests. These requests are meant to ensure the remote, on-premise VPN device is available and can maintain an active tunnel. Our diagnostic logs indicate your on-premise device stopped responding to Dead-Peer-Detection (DPD) requests. The next step in troubleshooting is to determine if you have logs from your on-premise device showing it was correctly responding to DPD requests. This will help us further diagnose the root cause of this issue.

Best Regards,
<!--/issueDescription-->