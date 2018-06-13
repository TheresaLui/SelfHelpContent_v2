<properties 
    pageTitle="Customer Public Prefixes Are Not Advertised From The Customer Edge"
    description="Customer Public Prefixes Are Not Advertised From The Customer Edge"
    infoBubbleText="Customer Public Prefixes Are Not Advertised From The Customer Edge.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    displayOrder=""
    articleId="ExRMsftPeeringCxPrefixesNotAdvDiag"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
 
# Microsoft Azure is unable to detect prefixes advertised from the customer edge <br>
A peering prefix is part of a BGP route used to advertise network reachability <br>
 
## Recommended steps
We recommend to check your peering status: <br>
In the Azure portal, the status of an ExpressRoute circuit can be checked by selecting "All Resources" on the left-side-bar menu and then selecting the ExpressRoute circuit. Selecting an ExpressRoute circuit listed under "All resources" will open the ExpressRoute circuit blade. In the "Overview" section of the blade, the ExpressRoute Essentials are shown, including Peerings.  <br>

Using PowerShell <br>
Get-AzureBGPPeering -AccessType Private -ServiceKey "*********************************" <br>
Get-AzureBGPPeering -AccessType Public -ServiceKey "*********************************" <br>
Get-AzureBGPPeering -AccessType Microsoft -ServiceKey "*********************************" <br>
 
## Recommended document
[Verifying Connectivity: Azure Express Route](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-troubleshooting-expressroute-overview) <br>
