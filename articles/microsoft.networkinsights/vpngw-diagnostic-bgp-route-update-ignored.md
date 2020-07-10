<properties
    pageTitle="BGP route update for prefix {prefix} was ignored because of overlapping or missing subnets"
    description="BGP route update for prefix {prefix} was ignored because of overlapping or missing subnets"
    infoBubbleText="Need more information about that issue? See details on the right."
    service="microsoft.network"
    resource="vaults"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    articleId="VPNGwBGPRouteIgnoredSubnet"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="Public, fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureVPNGateway"
/>

# BGP route update is ignored because of overlapping or missing subnets
<!--issueDescription-->
The BGP route update for prefix is ignored because it overlaps with local subnets or reserved subnets.
<!--/issueDescription-->

## **Recommended Steps**

Make sure the BGP routes aren't part of one of the VNet subnets or among reserved subnets.
