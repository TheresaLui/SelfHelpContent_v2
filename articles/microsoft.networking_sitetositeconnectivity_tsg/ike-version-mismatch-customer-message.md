<properties
pageTitle="IKE Version Mismatch"
description="IKE Version Mismatch"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="b7ef6771-5420-4983-8d67-679eccd5b276"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Version Mismatch

<!--issueDescription-->
Dear customer,

Thank you for contacting us regarding your Azure VPN Gateway connectivity issues. We've reviewed the logs and diagnostics available to us and have determined that your connectivity issue is due to an IKE version mismatch. If you are using a Policy Based Gateway, then please configure your gateway for IKEv1. If you're using a Route Based Gateway, please configure your gateway for IKEv2. If your connectivity issues persist after making these changes, then please contact us to troubleshoot further.

Best regards,
<!--/issueDescription-->