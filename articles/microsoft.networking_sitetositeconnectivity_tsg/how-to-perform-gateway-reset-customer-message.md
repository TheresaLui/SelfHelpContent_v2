<properties
pageTitle="How to perform gateway reset"
description="How to perform gateway reset"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="23733a6a-f727-4753-a660-02c5b9d3bddc"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# How to perform gateway reset

<!--issueDescription-->
Dear customer,

Thank you for contacting us regarding your VPN Gateway connectivity issue. If you're concerned about a sustained outage, we can perform a "gateway reset" which may immediately resolve the issue. While this may resolve your issue, it may mean we can not diagnose or root cause the issue further. If you'd like to immediately reset your VPN Gateway, then you can do via the Azure Portal or by using the following PowerShell command.

Reset-AzureVNetGateway -VNetname <name>

Best Regards,
<!--/issueDescription-->