<properties
	pageTitle="I can't connect to services deployed in my VNet"
	description="I can't connect to services deployed in my VNet"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="kasparks"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d4ba26f6-9bb3-49b0-8951-0437284d3bcf"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# I can't connect to services deployed in my VNet

## **Recommended steps**
To resolve the most common issues, try one or more of the following methods.

1. Check if a VPN Gateway is created.<br>
[Check if a VPN Gateway is created (type = ExpressRoute) for the virtual network](https://azure.microsoft.com/documentation/articles/expressroute-howto-add-gateway-resource-manager/)
2. Check connection between the VNet and the ExpressRoute circuit.<br>
Check if you have a connection between the VNet and the ExpressRoute circuit. Check if the connection is enabled.
3. Check layer 3 connectivity between your network and Microsoft.
	1. Get the route table summary for Azure private peering.
	2. Check if there are active BGP sessions between your routers and Microsoft's routers. You must have a pair of active BGP sessions (one primary and one secondary) between your network and Microsoft.
	3. Contact your service provider (if they manage routing for you to have any issues addressed).
	4. Check our router configuration samples for reference.
	5. If you manage routing, check if you have correct parameters.
		1. Check BGP neighbor IP addresses.
		2. Check your ASN (peer ASN) and the Azure ASN (12076).
		3. Check your MD5 hash (session key) if you configured one.
	6. Check if you have active BGP sessions between your VNets. You must have a pair of active BGP sessions for every VNet you connect to (with AS65515). BGP neighbor IPs will be private IP addresses in the gateway subnet of your VNet.
4. Check layer 3 connectivity up to your virtual network.
	1. Get the route table summary for Azure private peering.
	2. Check if there are active BGP sessions between your VNets. You must have a pair of active BGP sessions for every VNet you connect to (with AS65515). BGP neighbor IPs will be private IP addresses in the gateway subnet of your VNet.
5. Check if all the prefixes are advertised.
	1. Get the route table for Azure private peering.
	2. Check if all the required prefixes (on-premises and virtual networks) are present in the route table with appropriate next hops.

## **Recommended documents**
[For additional details, see following ExpressRoute Troubleshooting document](https://azure.microsoft.com/documentation/services/expressroute/)
