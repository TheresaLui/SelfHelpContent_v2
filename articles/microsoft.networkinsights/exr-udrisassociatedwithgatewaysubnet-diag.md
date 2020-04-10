<properties
pageTitle="A User Defined Route (UDR) Is Associated With GatewaySubnet"
description="A User Defined Route (UDR) Is Associated With GatewaySubnet"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors=""
displayOrder="10"
articleId="ExRVnetGatewayUdrOnGatewaySubnetInsight"
diagnosticScenario="ExRVnetGatewayUdrOnGatewaySubnetInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute Gateway Subnet Has UDR Applied
<!--issueDescription-->
We have identified that your gateway subnet for virtual network ID **<!--$VNetId-->[VNetId]<!--/$VNetId--> has the following user-defined route (UDR) associated: **<!--$UDRName-->[UDRName]<!--/$UDRName-->**. If the UDR has not been carefully configured you will experience connectivity issues to/from your virutal network resources or on-premises resources.
<!--/issueDescription-->
## **Steps to resolve the issue**

1. Use Network Watcher [Next Hop](https://docs.microsoft.com/azure/network-watcher/diagnose-vm-network-routing-problem) to verify if the subnet next hop is expected
2. Remove the route and test traffic flows
