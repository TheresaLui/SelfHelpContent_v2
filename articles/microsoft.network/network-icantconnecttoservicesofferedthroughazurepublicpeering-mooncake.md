<properties
    pageTitle="I can't connect to services offered through Azure Public peering"
    description="I can't connect to services offered through Azure Public peering"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="kasparks"
    ms.author="kasparks"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="b923ec3a-fd60-4145-9f90-d69441ca8c62"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# I can't connect to services offered through Azure Public peering

## **Recommended Steps**

To resolve most common issues, try one or more of the following steps:

1. Check layer 3 connectivity between your network and Microsoft:

    1. Get the route table summary for Azure public peering
    2. Check if there are active BGP sessions between your routers and Microsoft's routers. You must have a pair of active BGP sessions (one primary and one secondary) between your network and Microsoft.
    3. Contact your service provider (if they manage routing for you) to have any issues addressed
    4. Check our router configuration samples for reference
    5. If you manage routing, check if you have the correct parameters:

        1. Check BGP neighbor IP addresses
        2. Check your ASN (peer ASN) and the Azure ASN (12076)
        3. Check your MD5 hash (session key) if you configured one

2. Check if all the prefixes are advertised:

    1. Get the route table for Azure public peering
    2. Check if all the required prefixes are present in the route table with appropriate next hops

3. Check on-premises NAT configurations:

    1. Check NAT samples on Azure.com
    2. Check your NAT configuration

4. Check any on-premises Firewall Configuration
5. Check routing within your on-premises network to ensure that the routes are propagated appropriately

## **Recommended Documents**

* [ExpressRoute Troubleshooting](https://docs.azure.cn/expressroute/)
