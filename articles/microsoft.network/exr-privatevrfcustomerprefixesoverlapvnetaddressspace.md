<properties
    pageTitle="Customer Prefixes Overlap With VNet Address Space"
    description="Customer Prefixes Overlap With VNet Address Space"
    infoBubbleText="Customer Prefixes Overlap With VNet Address Space"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    displayOrder=""
    articleId="ExRPrivateVrfCustomerPrefixesOverlapVNetAddressSpaceInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# **Customer Prefixes Overlap With VNet Address Space**

**Message:** '**<!--$Message--> [Message] <!--/$Message-->**' 
**ServiceKey:** '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**' 
**MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**' 
**VRF Name:** '**<!--$VRF--> [VRF] <!--/$VRF-->**' 
**VnetID:** '**<!--$VNetId--> [VNetId] <!--/$VNetId-->**' 
**Gateway ID:** '**<!--$GatewayId--> [GatewayId] <!--/$GatewayId-->**' 

## **Recommended steps**

+ The customer should stop advertising the overlapping prefixes, or consider modifying the VNet address space.
+ Left as-is, the customer will experience unexpected routing behavior
