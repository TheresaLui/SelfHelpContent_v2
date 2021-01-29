<properties
pageTitle="ExpressRoute gateway subnet has UDR applied"
description="ExpressRoute gateway subnet has UDR applied"
infoBubbleText="Need more information about this issue? See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="TobyTu"
ms.author="pareshmu, mariliu"
displayOrder="10"
articleId="ExRVnetGatewayUdrOnGatewaySubnetInsight"
diagnosticScenario="ExRVnetGatewayUdrOnGatewaySubnetInsight"
selfHelpType="Diagnostics"
supportTopicIds="32627977"
resourceTags="windows"
productPesIds="15480"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute gateway subnet has UDR applied
<!--issueDescription-->
We have identified a user-defined route (UDR) in the gateway subnet of your ExpressRoute virtual network gateway **[Azure resource name]**. UDR with a 0.0.0.0/0 destination aren't supported. Gateways require access to the management controllers to function properly. BGP Route Propagation should be set to "enabled" on the GatewaySubnet to ensure the availability of the gateway. The gateway won't function if set to "disabled".
<!--/issueDescription-->
## **Steps to resolve the issue**

Remove the 0.0.0.0/0 default route from the gateway subnet.
