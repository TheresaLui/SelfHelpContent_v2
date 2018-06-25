<properties 
    pageTitle="Customer Public Prefixes Are Not Configured For The Peering"
    description="Customer Public Prefixes Are Not Configured For The Peering"
    infoBubbleText="Customer Public Prefixes Are Not Configured For The Peering.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    displayOrder=""
    articleId="ExRCxPubPrefixesNotConfForPeeringDiag"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# Microsoft Azure is unable to detect the Peering prefixes intended to be advertised to Microsoft
A peering prefix is part of a BGP route used to advertise network reachability.
 
## Recommended steps
We recommend that you recreate the peering and specify which public prefixes you intend to advertise to Microsoft. <br>
In the Azure portal, select "All Resources" on the left-side-bar menu and then select the ExpressRoute circuit. <br>
Selecting an ExpressRoute circuit listed under "All resources" will open the ExpressRoute circuit blade. <br> 
In the "Overview" section of the blade, the ExpressRoute Essentials are shown.  <br>
From there you will be able to configure your peerings.

## Recommended document
[Verifying Connectivity: Azure Express Route](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview) <br
