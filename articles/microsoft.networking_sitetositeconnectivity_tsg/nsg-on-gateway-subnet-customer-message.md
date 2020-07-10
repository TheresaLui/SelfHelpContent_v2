<properties
pageTitle="NSG on VPN Gateway subnet is blocking connectivity"
description="NSG on VPN Gateway subnet is blocking connectivity"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="bf706ead-dd28-4e9a-9df4-c4720a83b138"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# NSG on VPN Gateway subnet is blocking connectivity

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We've reviewed the logs and diagnostics available to us and have determined that your issue is due to an NSG on the gateway subnet. To resolve this issue, please add the tag "GatewayManager" on VPN Gateway Subnet. This will apply the necessary NSG rules that will allow traffic required for the VPN Gateway. Alternatively, you may remove the NSG from the gateway subnet.

Best regards,
<!--/issueDescription-->