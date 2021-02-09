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

# ExpressRoute Gateway Subnet has UDR Applied
<!--issueDescription-->
We have identified user-defined routes (UDR) <!--$UDRStrings-->**UDRStrings** <!--/$UDRStrings--> in the gateway subnet of your ExpressRoute virtual network gateway <!--$GatewayName-->**GatewayName**<!--/$GatewayName-->. UDR with a 0.0.0.0/0 destination in the gateway subnet are not supported.
<!--/issueDescription-->
## **Steps to Resolve Issue:**

Remove the 0.0.0.0/0 default route from the gateway subnet.
