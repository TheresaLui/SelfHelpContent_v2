<properties
    pageTitle="Configure caching"
    description="Configure caching"
    service="microsoft.afd"
    resource="afd"
    authors="jtwalters25" 
    ms.author="jewalte"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32614241"
    resourceTags=""
    productPesIds="16611"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c9e77afb-2a5d-474e-be70-585dc792b54b"
	ownershipId="CloudNet_AzureFrontdoor"
/>

# Configure Caching

Azure Front Door Service can deliver large files without a cap on file size using a technique called "object chunking". When a large file is requested, Front Door retrieves smaller pieces of the file from the backend. After receiving a full or byte-range file request, a Front Door environment requests the file from the backend in chunks of 8 MB. The recommended documents listed below will provide instructions on configuring caching for your Front Door service.

## **Recommended Documents**

* [Caching with Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/front-door-caching)
* [How to create a Front Door with caching enabled](https://azure.microsoft.com/resources/templates/201-front-door-create-caching/) for a defined routing configuration that will cache static assets for your work

