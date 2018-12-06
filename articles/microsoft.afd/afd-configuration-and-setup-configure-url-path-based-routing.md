<properties
    pageTitle="Configure URL path-based routing"
    description="Configure URL path-based routing"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25" authorAlias="jewalte"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614246"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public"
/>

# Configure URL Path Based Routing

URL Path Based Routing allows you to route traffic to backend pools based on URL paths of the request. A common scenario is to route requests for different content types to specific backend pools. In this configuration, Front Door will match based on HTTP protocol, then Frontend host, then the Path.

## **Recommended Documents**
* [Enforce URL-based routing](https://docs.microsoft.com/azure/frontdoor/front-door-overview#url-based-routing) 
* [Match a given Front Door routing rule](https://docs.microsoft.com/azure/frontdoor/front-door-route-matching#route-matching) 

