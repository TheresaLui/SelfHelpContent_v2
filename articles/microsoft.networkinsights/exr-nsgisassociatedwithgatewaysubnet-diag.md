<properties
pageTitle="A Network Security Group (NSG) Is Associated With GatewaySubnet"
description="A Network Security Group (NSG) Is Associated With GatewaySubnet"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors=""
displayOrder="10"
articleId="ExRVnetGatewayNsgOnGatewaySubnetInsight"
diagnosticScenario="ExRVnetGatewayNsgOnGatewaySubnetInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute Gateway Subnet Has NSG Applied
<!--issueDescription-->
We have identified that your gateway subnet for virtual network ID **<!--$VNetId-->[VNetId]<!--/$VNetId--> has the following NSG associated: **<!--$NSGName-->[NSGName]<!--/$NSGName-->**. If the NSG has not been carefully configured you will experience connectivity issues to/from your virutal network resources or on-premises resources.
<!--/issueDescription-->
## **Steps to resolve the issue**

1. [Delete the NSG](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group#delete-a-network-security-group) from the Application Gateway subnet and test communication.
2. Use [IP Flow](https://docs.microsoft.com/azure/network-watcher/network-watcher-ip-flow-verify-overview) to verify NSG rules allow traffic flow in both directions.
