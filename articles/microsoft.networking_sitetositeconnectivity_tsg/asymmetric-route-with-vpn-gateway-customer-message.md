<properties
pageTitle="Asymmetric Routing with VPN Gateway Customer Message"
description="Asymmetric Routing with VPN Gateway Customer Message"
infoBubbleText= "Issues with your Site to Site VPN Connectivity were detected. See details on the right."
service="microsoft.network"
resource="vpnGateways"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="e8c9fe5f-ade8-4594-831a-91bd4e248582"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32591158,32584882,32584881"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureVPNGateway"
/>

# Asymmetric Routing with VPN Gateway Insight

<!--issueDescription-->
Dear customer,
Thank you for working with us to identify the cause of the issue you are experiencing. We believe this issue to be caused by asymmetric routing. In this specific example, connection attempts between your on-premise device and VPN Gateway would take one both and the return traffic would take another path, leading to those connection attempts being dropped by an intermediary network device, such as an on-premise firewall. This [document](https://docs.microsoft.com/azure/expressroute/expressroute-asymmetric-routing) describes more about what asymmetric routing and offers some suggestions on how to remediate.

We recommend having the public IP address of your VPN gateway and the IP address of your on-prem gateway be advertised through the same routing path (either the Internet or via ExpressRoute).

Please let us know if you need any further assistance on this matter.

Best Regards
<!--/issueDescription-->