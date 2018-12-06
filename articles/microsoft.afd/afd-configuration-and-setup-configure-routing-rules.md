<properties
    pageTitle="Configure routing rules"
    description="Configure routing rules"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25" 
    authorAlias="jewalte"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614244"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public"
/>

# Configure Routing Rules

After establishing a connection and doing an SSL handshake, Front Door will determine which particular routing rule to match the incoming request to. If there are no routing rules for an exact match front end host with a catch-all route Path, there will be no match to any routing rule.

## **Recommended Documents**

* Front Door route configuration and how [Front Door matches requests to a routing rule](https://docs.microsoft.com/azure/frontdoor/front-door-route-matching)
* Configuring [Front Door to enable Azure managed application firewall ruleset](https://azure.microsoft.com/resources/templates/201-front-door-managed-waf-ruleset/)
