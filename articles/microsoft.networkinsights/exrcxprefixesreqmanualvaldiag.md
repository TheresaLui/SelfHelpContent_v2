<properties 
    pageTitle="Customer Prefixes Require Manual Validation"
    description="Customer Prefixes Require Manual Validation"
    infoBubbleText="Customer Prefixes Require Manual Validation.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    displayOrder=""
    articleId="exrcxprefixesreqmanualvaldiag"
    selfHelpType="diagnostics"
    supportTopicIds="32539943, 32586802, 32539944"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# Microsoft Azure is unable to automatically validate your Public Prefix
Peering for ExpressRoute requires customer-supplied public prefixes are verified against a registrar, such as ARIN.  This is a standard practice to verify identity and ownership of IP address space.

## Recommended steps
1.  This likely failed due to the **OriginAS** property being null at the registry. <br>
2.  To avoid this issue in the future, please consider updating your Organization information at <br>
the registry so the OriginAS is populated with an appropriate ASN <br>

## **Recommended documents**
[Create and modify peering for an ExpressRoute circuit](https://docs.microsoft.com/azure/expressroute/expressroute-howto-routing-portal-resource-manager)
