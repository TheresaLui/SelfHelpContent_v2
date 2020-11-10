<properties
	pageTitle="I can't connect to services offered through Microsoft peering"
	description="I can't connect to services offered through Microsoft peering"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="kasparks"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="57e519cb-eb8d-48aa-8160-292f8238c05b"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# I can't connect to services offered through Microsoft peering

## **Recommended steps**
To resolve the most common issues, try one or more of the following methods.

1. Check layer 3 connectivity between your network and Microsoft.
	1. Get the route table summary for Microsoft peering.
	2. Check if there are active BGP sessions between your routers and Microsoft's routers. You must have a pair of active BGP sessions (one primary and one secondary) between your network and Microsoft.
	3. Contact your service provider (if they manage routing for you to have any issues addressed).
	4. Check our router configuration samples for reference.
	5. If you manage routing, check if you have correct parameters.
		1. Check BGP neighbor IP addresses.
		2. Check your ASN (peer ASN) and the Azure ASN (12076).
		3. Check your MD5 hash (session key) if you configured one.
2. Check prefix list.
	1. Check if you have provided the correct list of prefixes to be advertised into Microsoft.
	2. Check if you have specified the correct routing registry name.
	3. Check if the prefixes are all auto-validated.
	4. Open a support ticket to have your prefixes validated. Provide proof of ownership of prefixes.
3. Check if all the prefixes are advertised.
	1. Get the route table for Azure public peering.
	2. Check if all the required prefixes are present in the route table with appropriate next hops.
4. Check on-premises NAT configurations.
	1. Check NAT samples on Azure.com
	2. Check your NAT configuration.
5. Check Firewall.<br>
Check on-premises Firewall Configuration.
6. Check routing.<br>
Check routing within your on-premises network to ensure that the routes are propagated appropriately.

## **Recommended documents**
[For additional details, see following ExpressRoute Troubleshooting document](https://azure.microsoft.com/documentation/services/expressroute/)
