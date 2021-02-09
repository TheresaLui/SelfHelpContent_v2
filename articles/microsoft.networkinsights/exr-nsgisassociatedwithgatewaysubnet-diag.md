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

# ExpressRoute Gateway Subnet has NSG Applied
<!--issueDescription-->
We have identified a network security group (NSG) **<!--$NSGName-->NSGName<!--/$NSGName-->** in the gateway subnet of your ExpressRoute virtual network gateway **<!--$GatewayName-->GatewayName<!--/$GatewayName-->**. Gateways require access to the management controllers to function properly. BGP Route Propagation must be set to "enabled" on the GatewaySubnet to ensure the availability of the gateway. If this is set to "disabled", the gateway will not function.
<!--/issueDescription-->
## **Steps to Resolve the Issue:**

Remove the NSG that is blocking access to the management controllers.
