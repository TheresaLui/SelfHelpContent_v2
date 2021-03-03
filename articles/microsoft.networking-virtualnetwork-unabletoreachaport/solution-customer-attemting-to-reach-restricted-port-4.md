<properties
	  pageTitle="Customer attemting to reach restricted port"
	  description="Customer attemting to reach restricted port"
      service="Microsoft.network"
      resource="Microsoft.network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="22dcb30a-e08f-472c-8c67-19204ab439ce"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Customer attemting to reach restricted port

<!--issueDescription-->

The current port you are attempting to reach is restricted by Azure.

You can use TCP, UDP, and ICMP TCP/IP protocols within VNets. Unicast is supported within VNets, with the exception of Dynamic Host Configuration Protocol (DHCP) via Unicast (source port UDP/68 / destination port UDP/67) and UDP source port 65330 which is reserved for the host. Multicast, broadcast, IP-in-IP encapsulated packets, and Generic Routing Encapsulation (GRE) packets are blocked within VNets.


<!--/issueDescription-->

