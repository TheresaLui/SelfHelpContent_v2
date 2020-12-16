<properties
pageTitle="A Network Security Group (NSG) Is Associated With GatewaySubnet"
description="A Network Security Group (NSG) Is Associated With GatewaySubnet"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="TobyTu"
ms.author="pareshmu, mariliu"
displayOrder="10"
articleId="ExRVnetGatewayNsgOnGatewaySubnetInsight"
diagnosticScenario="ExRVnetGatewayNsgOnGatewaySubnetInsight"
selfHelpType="Diagnostics"
supportTopicIds="32627977"
resourceTags="windows"
productPesIds="15480"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute gateway subnet has NSG applied
<!--issueDescription-->
We have identified a network security group (NSG) in the gateway subnet of your ExpressRoute virtual network gateway **[Azure resource name]**. Gateways require access to the management controllers to function properly. BGP Route Propagation must be set to "enabled" on the GatewaySubnet to ensure the availability of the gateway. The gateway won't function if set to "disabled".
<!--/issueDescription-->
## **Steps to resolve the issue**

Remove the NSG that is blocking access to the management controllers.
