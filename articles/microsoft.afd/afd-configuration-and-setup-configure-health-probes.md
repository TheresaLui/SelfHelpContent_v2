<properties
    pageTitle="Configure health probes"
    description="Configure health probes"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25"
    ms.author="jewalte"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614243"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="8499e1cb-dd26-43ef-beb2-969863ba8570"
	ownershipId="CloudNet_AzureFrontdoor"
/>

# Configure Health Probes

In order to determine the health of each backend, each Front Door environment periodically sends a synthetic HTTP/HTTPS request to your configured backends. Front Door then uses responses from these probes to determine the "best" backends to which it should route real client requests.

Front Door supports sending probes over HTTP or HTTPS protocols. These probes are sent over the same TCP ports configured for routing client requests, and cannot be overridden.

## **Recommended Documents**

* [Control Health Probes](https://docs.microsoft.com/azure/frontdoor/front-door-health-probes)
* A brief explanation of [Azure Front Door's health probe](https://azure.microsoft.com/resources/templates/201-front-door-health-probes/) concept and the supported protocols

