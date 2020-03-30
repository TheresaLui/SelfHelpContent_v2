<properties
    pageTitle="I can't connect to services deployed in my VNet"
    description="I can't connect to services deployed in my VNet"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="kasparks"
    ms.author="kasparks"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="2a8bc337-8821-4d1b-be22-c48ac3601082"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# I can't connect to services deployed in my VNet

## **Recommended Steps**

To resolve the most common issues, try one or more of the following methods:

1. Check if a [VPN Gateway is created](https://docs.azure.cn/expressroute/expressroute-howto-add-gateway-resource-manager/)
2. Check connection between the VNet and the ExpressRoute circuit and ensure it is enabled
3. Check layer 3 connectivity between your network and Microsoft:

    1. Get the route table summary for Azure private peering
    2. Check if there are active BGP sessions between your routers and Microsoft's routers. You must have a pair of active BGP sessions (one primary and one secondary) between your network and Microsoft.
    3. Contact your service provider (if they manage routing for you) to have any issues addressed
    4. Check our router configuration samples for reference
    5. If you manage routing, check if you have correct parameters:

        1. Check BGP neighbor IP addresses
        2. Check your ASN (peer ASN) and the Azure ASN (12076)
        3. Check your MD5 hash (session key) if you configured one

    6. Check if you have active BGP sessions between your VNets. You must have a pair of active BGP sessions for every VNet you connect to (with AS65515). BGP neighbor IPs will be private IP addresses in the gateway subnet of your VNet.

4. Check layer 3 connectivity up to your virtual network:

    1. Get the route table summary for Azure private peering
    2. Check if there are active BGP sessions between your VNets. You must have a pair of active BGP sessions for every VNet you connect to (with AS65515). BGP neighbor IPs will be private IP addresses in the gateway subnet of your VNet.

5. Check if all the prefixes are advertised:

    1. Get the route table for Azure private peering
    2. Check if all the required prefixes (on-premises and virtual networks) are present in the route table with appropriate next hops

## **Recommended Documents**

* [ExpressRoute Troubleshooting](https://docs.azure.cn/expressroute/)
