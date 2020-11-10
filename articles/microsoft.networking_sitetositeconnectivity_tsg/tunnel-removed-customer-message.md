<properties
pageTitle="VPN Gateway connection object was deleted"
description="VPN Gateway connection object was deleted"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="0cae12aa-a263-4642-9e6b-4773770d25e6"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# VPN Gateway connection object was deleted

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your Azure VPN Gateway connectivity issue. We've reviewed the logs and diagnostics available to us and have determined that your connectivity issue is the result of the VPN Gateway connection object being deleted. The connection object can only be deleted by someone with access to your Azure configuration, most likely be someone within your organization. When the connection object is deleted, then the VPN Gateway, by design, will disconnect any active tunnel. Please re-configure a connection object in order to establish VPN connectivity.

Best regards,
<!--/issueDescription-->