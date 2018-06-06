<properties 
    pageTitle="Customer Prefixes Require Manual Validation"
    description="Customer Prefixes Require Manual Validation"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="krisney"
    displayOrder=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
 
# Microsoft Azure is unable to automatically validate your Public Prefix <br>
Peering for ExpressRoute requires customer-supplied public prefixes are verified against a registrar, such as ARIN <br>
This is a standard practice to verify identity and ownership of IP address space.

## Recommended steps
1.  This likely failed due to the **OriginAS** property being null at the registry. <br>
2.  To avoid this issue in the future, please consider updating your Organization information at <br>
the registry so the OriginAS is populated with an appropriate ASN <br>
## Recommended document
[Create and modify peering for an ExpressRoute circuit](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-howto-routing-portal-resource-manager) <br>
