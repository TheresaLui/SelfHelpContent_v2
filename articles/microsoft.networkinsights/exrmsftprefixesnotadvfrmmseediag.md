<properties 
    pageTitle="Microsoft Prefixes Are Not Advertised From The MSEE"
    description="Microsoft Prefixes Are Not Advertised From The MSEE"
    infoBubbleText="Microsoft Prefixes Are Not Advertised From The MSEE.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    displayOrder=""
    articleId="ExRMicrosoftPeeringMicrosoftPrefixesIpv4NotAdvertisedInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>
# Microsoft IPv4 Peering Prefixes are not Advertised
This is likely failing due to missing route filters.  Many services are accessible through peering configured on an Express Route circuit.  The prefixes related to those services are advertised through Border Gateway Protocol (BGP) session that are established.  A BGP community value is attached to every prefix to identify the service that is offered through the prefix. <br> 
<br>
When peering is configured on your ExpressRoute circuit, the Microsoft edge routers establish a pair of BGP sessions with the edge routers (yours or your connectivity provider's). No routes are advertised to your network. <br> 
<br>
To enable route advertisements to your network, you must associate a route filter.<br>
<br>
A route filter lets you identify services you want to consume through your ExpressRoute circuit's Microsoft peering. It is essentially a white list of all the BGP community values.  Once a route filter resource is defined and attached to an ExpressRoute circuit, all prefixes that map to the BGP community values are advertised to your network.
 
## **Recommended steps**
Please check for/create route filters that you wish to consume <br>
Once route filters are created, prefixes should populate from the Microsoft edge to the your device.

## **Recommended document**
[Configure route filters for Microsoft Peering](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-portal) <br>
