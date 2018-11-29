<properties 
    pageTitle="Customer Public Prefixes Are Not Advertised From The Customer Edge"
    description="Customer Public Prefixes Are Not Advertised From The Customer Edge"
    infoBubbleText="Customer Public Prefixes Are Not Advertised From The Customer Edge.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    displayOrder=""
    articleId="ExRMicrosoftPeeringCustomerPrefixesNotAdvertisedInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# Microsoft Azure is unable to detect prefixes advertised from the customer edge <br>
A peering prefix is part of a BGP route used to advertise network reachability <br>
 
## **Recommended steps**
We recommend to check your peering status, you can check this in the portal or using PowerShell: <br>
Using Portal:<br>
1)  In the Azure portal select "All Resources" <br>
2)  Select the "ExpressRoute circuits" to launch the ExpressRoute circuit blade <br>
3)  In the "Overview" section of the blade, the ExpressRoute Essentials are shown <br>
4)  Click on "Peerings" to check the status of the peering <br>

Using PowerShell <br>
Get-AzureBGPPeering -AccessType Private -ServiceKey "*********************************" <br>
Get-AzureBGPPeering -AccessType Public -ServiceKey "*********************************" <br>
Get-AzureBGPPeering -AccessType Microsoft -ServiceKey "*********************************" <br>
 
## **Recommended document**
[Verifying Connectivity: Azure Express Route](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview) <br>
