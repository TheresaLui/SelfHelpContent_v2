<properties
    pageTitle="Customer Prefixes Overlap With VNet Address Space"
    description="Customer Prefixes Overlap With VNet Address Space"
    infoBubbleText="Customer Prefixes Overlap With VNet Address Space"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    ms.author="pareshmu"
    displayOrder=""
    articleId="ExRPrivateVrfCustomerPrefixesOverlapVNetAddressSpaceInsight"
    selfHelpType="diagnostics"
    diagnosticScenario="ExRPrivateVrfCustomerPrefixesOverlapVNetAddressSpaceInsight"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# **Customer Prefixes Overlap With VNet Address Space**
<!--/issueDescription-->
* **Message:** '**<!--$Message--> [Message] <!--/$Message-->**'
* **ServiceKey:** '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**'
* **MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**'
* **VRF Name:** '**<!--$VRF--> [VRF] <!--/$VRF-->**'
* **VnetID:** '**<!--$VNetId--> [VNetId] <!--/$VNetId-->**'
* **Gateway ID:** '**<!--$GatewayId--> [GatewayId] <!--/$GatewayId-->**'
<!--/issueDescription-->

## **Recommended Steps**

+ The customer should stop advertising the overlapping prefixes, or consider modifying the VNet address space
+ If left as-is, the customer will experience unexpected routing behavior

## **Recommended Documents**

* [Microsoft cloud services and network security best practices](https://docs.microsoft.com/azure/best-practices-network-security)
* [Optimize ExpressRoute Routing](https://docs.microsoft.com/azure/expressroute/expressroute-optimize-routing)
