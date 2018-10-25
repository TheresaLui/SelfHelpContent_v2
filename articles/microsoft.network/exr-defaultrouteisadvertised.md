<properties 
    pageTitle="ExpressRoute: DefaultRoute Is Advertised"
    description="ExpressRoute: DefaultRoute Is Advertised"
    infoBubbleText="ExpressRoute: DefaultRoute Is Advertised"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    displayOrder=""
    articleId="ExpressRouteDefaultRouteIsAdvertised"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
## **Default Routes Advertised**
ExpressRoute circuit: '**<!--$CircuitName-->[CircuitName]<!--/$CircuitName-->**' 
Default Route is advertised
 
## **Recommended steps**
Review '**<!--$$DumpRoutingInfo-->[Dump Routing Info]<!--/$DumpRoutingInfo-->**' for details. 

Customer advertising default routes causes all traffic from Azure to go back to customer on-premises.
Ensure the traffic behavior of peering(s) for which the default route is advertised is not adversely affected by the route advertisement. If the route advertisement is causing undesirable traffic behavior, ask the customer to consider removing the route advertisement.

## **Recommended document**
[Advertising Default Routes](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-routing#advertising-default-routes) <br>

