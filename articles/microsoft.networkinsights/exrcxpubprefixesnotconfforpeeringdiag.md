<properties
    pageTitle="Customer Public Prefixes Are Not Configured For The Peering"
    description="Customer Public Prefixes Are Not Configured For The Peering"
    infoBubbleText="Customer Public Prefixes Are Not Configured For The Peering.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    ms.author="krisney"
    displayOrder=""
    articleId="ExRMicrosoftPeeringCustomerPrefixesNotFoundInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>
# Microsoft Azure is unable to detect the Peering prefixes intended to be advertised to Microsoft
<!--/issueDescription-->
Peering is an agreement to interconnect and exchange routing information.  A peering prefix is part of a BGP route used to advertise network reachability.  When a peering session cannot be established, routing information cannot be exchanged and data cannot transit the connection.  
 <!--/issueDescription-->

## **Recommended Steps**

We recommend that you recreate the peering and specify which public prefixes you intend to advertise to Microsoft.

* In the Azure portal, select "All resources" on the left-side-bar menu and then select the ExpressRoute circuit
* Selecting an ExpressRoute circuit listed under "All resources" will open the ExpressRoute circuit blade
* In the "Overview" section of the blade, the ExpressRoute Essentials are shown
* Click on "Peerings" to configure peerings for your ExpressRoute circuit

## **Recommended Documents**

* [Verifying Connectivity: Azure Express Route](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview)
