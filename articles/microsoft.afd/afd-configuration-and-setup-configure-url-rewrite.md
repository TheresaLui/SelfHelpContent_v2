<properties
    pageTitle="Configure URL rewrite"
    description="Configure URL rewrite"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25" 
    authorAlias="jewalte"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614247"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public"
/>

# Configure URL Rewrite

Azure Front Door Service supports URL rewrite, allowing you to configure an optional Custom Forwarding Path to use when constructing the request to forward to the backend. By default, if no custom forwarding path is provided, then Front Door will copy the incoming URL path to the URL used in the forwarded request. The Host header used in the forwarded request is as configured for the selected backend.

## **Recommended Documents**

* [Create a URL rewrite](https://docs.microsoft.com/azure/frontdoor/front-door-url-rewrite) 
* [Backend Host Header](https://docs.microsoft.com/azure/frontdoor/front-door-backend-pool#hostheader)

