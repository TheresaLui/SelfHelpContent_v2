<properties
pageTitle="Connection failure due to no response to gateway keep alive pings"
description="Connection failure due to no response to gateway keep alive pings"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="09f0bde8-a04e-410a-97ca-66013f143150"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# Connection failure due to no response to gateway keep alive pings

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your VPN Gateway connectivity issues. We've checked diagnostic logs for your VPN device and have determined this issue is a result of your on-premise VPN device not properly handling "Gateway Ping Tasks" which are meant to prevent the VPN connection from timing out after a five minute idle period. One option for remediation is to disable the "Gateway Ping Task" on the Azure VPN Gateway or you can consider remediation options for your on-premise VPN device.

Best Regards,
<!--/issueDescription-->