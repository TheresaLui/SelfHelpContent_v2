<properties
	  pageTitle="Ensure the customer is not attempting to reach a restricted port."
	  description="Ensure the customer is not attempting to reach a restricted port."
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
	  articleId="70aa413c-17c2-489f-a51a-d32a4465a248"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Ensure the customer is not attempting to reach a restricted port.

You can use TCP, UDP, and ICMP TCP/IP protocols within VNets. Unicast is supported within VNets, with the exception of Dynamic Host Configuration Protocol (DHCP) via Unicast (source port UDP/68 / destination port UDP/67) and UDP source port 65330 which is reserved for the host. Multicast, broadcast, IP-in-IP encapsulated packets, and Generic Routing Encapsulation (GRE) packets are blocked within VNets.


#Recommended Steps

1. Confirm with customer what ports the issue is with.

2. Confirm issue is not with one of the above motioned ports. 



