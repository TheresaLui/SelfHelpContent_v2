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

# Configure URL path-based routing

* URL Path Based Routing allows you to route traffic to backend pools based on URL paths of the request. One of the scenarios is to route requests for different content types to different backend pools.

## **Recommended documents**
* Learn [how to enforce URL-based routing.](https://review.docs.microsoft.com/azure/frontdoor/front-door-overview?branch=master#url-based-routing) Which allows you to route traffic to backend pools based on URL paths of the request.<br>
* This section will focus on  [how to match to a given Front Door routing rule.](https://docs.microsoft.com/azure/frontdoor/front-door-route-matching#route-matching) The basic concept is that we always match to the most-specific match first looking only at the "left-hand side". We first match based on HTTP protocol, then Frontend host, then the Path.<br>

