<properties
    pageTitle="Configure URL path-based routing"
    description="Configure URL path-based routing"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614246"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public"
/>

# Configure URL path-based routing

## **Recommended documents**
* Learn [how to enforce URL-based routing.](https://review.docs.microsoft.com/azure/frontdoor/front-door-overview?branch=master#url-based-routing) which  allows you to route traffic to backend pools based on URL paths of the request.<br>
* This section will focus on  [how to match to a given Front Door routing rule.](https://docs.microsoft.com/azure/frontdoor/front-door-route-matching#route-matching) The basic concept is that we always match to the most-specific match first looking only at the "left-hand side". We first match based on HTTP protocol, then Frontend host, then the Path.<br>

