<properties
	  pageTitle="Check ExR connectivity"
	  description="Check ExR connectivity"
	service="Microsoft.Network"
resource="Microsoft.network/virtualWans,Microsoft.Network/virtualwans,Microsoft.Network/virtualWans"
	  authors="lochiluk"
	  ms.author="Brwurz"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="b17bf652-1812-474b-b472-a98456108215"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Check ExR connectivity

In this step you'll be looking into the child gateway and see if the tunnel is up/connected by using steps below:

Check the ARP info as you usually do it for Expressroute case.
1) Pull the Dump routing info and search for BGP Info. 
2) Start looking for AS numbers by scrolling down and find the Customer's AS numbers. (Ignore 12076 (MSEE device AS path) &  65515 (Azure Gateway AS path) ) 
3) Once you find customers AS Path, in the same section check for State: Established. 
4) Finally, check for the source and destination address prefixes in the Dump routing info.

