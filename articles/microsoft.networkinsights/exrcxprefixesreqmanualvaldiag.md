<properties
    pageTitle="Customer Prefixes Require Manual Validation"
    description="Customer Prefixes Require Manual Validation"
    infoBubbleText="Customer Prefixes Require Manual Validation.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    ms.author="krisney"
    displayOrder=""
    articleId="ExRMicrosoftPeeringCustomerPrefixesRequireValidationInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32539943, 32586802, 32539944"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>
# Microsoft Azure is unable to automatically validate your Public Prefix
<!--/issueDescription-->
Peering for ExpressRoute requires customer-supplied public prefixes are verified against a registrar, such as ARIN.  This is a standard practice to verify identity and ownership of IP address space.
<!--/issueDescription-->

## **Recommended Steps**

* This likely failed due to the **OriginAS** property being null at the registry
* To avoid this issue in the future, please consider updating your organization information at the registry so the OriginAS is populated with an appropriate ASN

## **Recommended Documents**

* [Create and modify peering for an ExpressRoute circuit](https://docs.microsoft.com/azure/expressroute/expressroute-howto-routing-portal-resource-manager)
