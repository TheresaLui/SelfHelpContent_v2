<properties
    pageTitle="Cookie based session affinity"
    description="Cookie based session affinity"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25" 
    ms.author="jewalte"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614249"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="8afd345c-8a37-4139-b7bd-ee919945a6c8"
	ownershipId="CloudNet_AzureFrontdoor"
/>

# Session Affinity

By default, without session affinity, Front Door forwards requests originating from the same client to different backends based on load balancing configuration, particularly as the latencies to different backends change or if different requests from the same user lands on a different Front Door environment. However, some stateful applications or in certain other scenarios, prefer that subsequent requests from the same user land on the same backend that processed the initial request. The cookie-based session affinity feature is useful when you want to keep a user session on the same backend. By using Front Door-managed cookies, Azure Front Door Service can direct subsequent traffic from a user session to the same backend for processing as long as the backend is healthy and the user session hasn't expired.

Session affinity can be enabled at a frontend host level that is for each of your configured domains (or subdomains). Once enabled, Front Door adds a cookie to the user's session. Cookie-based session affinity allows Front Door to identify different users even if behind the same IP address, which in turn allows a more even distribution of traffic between your different backends.

The lifetime of the cookie is the same as the user's session, as Front Door currently only supports session cookie.

## **Recommended Documents**
* [Session affinity and Front door routing methods](https://docs.microsoft.com/azure/frontdoor/front-door-routing-methods#latency)
* Enable [session affinity for your Front End host](https://azure.microsoft.com/resources/templates/201-front-door-session-affinity/) 

