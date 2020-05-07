<properties
pageTitle="VPN configuration exceeding maxmimum number of supported SAs"
description="VPN configuration exceeding maxmimum number of supported SAs"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="52a5ff7f-3d00-40ee-97c6-80791a57e54a"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# VPN configuration exceeding maxmimum number of supported SAs

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We've reviewed the logs and diagnostics available to us and have determined that your connectivity issue is the result of exceeding the maximum number of SAs supported by Azure VPN Gateway (200 SAs). The total number of SAs can be calculated by multiplying the number of Azure Vnet Subnets by the number of local subnets defined in the local network gateway. Unfortunately, there is no workaround for this and 200 is a hard maximum limit.

Best regards,
<!--/issueDescription-->