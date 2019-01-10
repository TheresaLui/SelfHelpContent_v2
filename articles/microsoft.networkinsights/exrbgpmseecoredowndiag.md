<properties 
	pageTitle="BGP Peering Between MSEE and Microsoft Core Router Is Down"
	description="BGP Peering Between MSEE and Microsoft Core Router Is Down"
	infoBubbleText="BGP Peering issue found. See details on the right."
	service="microsoft.network"
	resource="ExpressRoute"
	authors="KristinaNeyens"
	displayOrder=""
	articleId="ExRCoreRouterBgpPeeringToMseeIsDownInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32539944, 32539949, 32539954"
	resourceTags="expressroute"
	productPesIds="15480"
	cloudEnvironments="public"
	/>
# BGP Peering Between MSEE and Microsoft Core Router Is Down
Microsoft Azure has identified an issue between the MSEE (Microsoft Enterprise Edge router) and the service provider where your ExpressRoute circuit is provisioned. An MSEE is the Microsoft Datacenter side of the network connection which connects to the service provider side routers/switches that are necessary to create the network connection. Border Gateway Protocol (BGP) is the routing protocol used to provide routing information to direct the traffic. When BGP peering between two endpoints is down, traffic is not able to transit the network path.
## **Recommended steps**
We are actively working to resolve the issue and you can receive updates by subscribing to Service Health Alerts using [service health alerts documentation](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-activity-log-alerts-on-service-notifications?toc=%2fazure%2fservice-health%2ftoc.json), or view your peering status from the portal following below steps: <br>
	1. On the left pane choose "All services" <br>
	2. Select "ExpressRoute circuits" <br>
	3. Once the circuit is selected, you should see Peerings on the bottom left where you can check the status
