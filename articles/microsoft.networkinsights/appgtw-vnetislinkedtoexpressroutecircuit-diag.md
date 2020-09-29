<properties
pageTitle="Application Gateway VNet is Linked to ExpressRoute Circuit"
description="Application Gateway VNet is Linked to ExpressRoute Circuit"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="ApplicationGatewayVNetisLinkedtoExpressRouteCircuit"
diagnosticScenario="ApplicationGatewayVNetisLinkedtoExpressRouteCircuit"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Microsoft Azure has identified Application Gateway exists in a Vnet linked to an ExpressRoute Circuit
<!--issueDescription-->
We have identified that your Application Gateway: **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->** in Subnet: **<!--$SubnetName-->[SubnetName]<!--/$SubnetName-->** in VNet:**<!--$VnetName--> [VnetName]<!--/$VnetName-->** is linked to ExpressRoute circuit: **<!--$ExpressRouteCircuit-->[ExpressRouteCircuit]<!--/$ExpressRouteCircuit-->**. If a default route is advertised from your on-premises you may have issues accessing the solution behind your application gateway or the backend health may be affected because the probe traffic is getting rerouted to your on-premises.
<!--/issueDescription-->
## **Steps to resolve routing issues**
Ensure the ExpressRoute circuit link and routes are not preventing traffic to or from the Application Gateway. You can use [Network Watcher 'Next Hop'](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview) to validate this.
If you are broadcasting a default route over your ExpressRoute you will need to [create a user-defined route](https://docs.microsoft.com/azure/virtual-network/manage-route-table#create-a-route-table) to your Application Gateway subnet with next hop **Internet**. This will allow the Application Gateway probes to reach the Application Gateway backend pool resources and receive their response ensuring a working solution.
