<properties
	  pageTitle="Review packet captures to see if traffic is seen passing the gateway."
	  description="Review packet captures to see if traffic is seen passing the gateway."
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
	  articleId="ef00042a-fb8a-47c5-a3aa-f2f583ac18bd"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Review packet captures to see if traffic is seen passing the gateway.

Seeing the traffic from the source pass through the VPN gateway lets us know that the traffic is now inside of Azure. 
?
#Recommended Steps
	1. Filter the packet capture for traffic between the IP addresses of the source and destination. See documentation for details on setting filters if needed. 
	2. Search to see if you can see traffic that contains the source IP used for the test in the source column going to the tested destination IP address. 
?
#Reccommended Documents
?
	1. (Wireshark Filters)[https://wiki.wireshark.org/DisplayFilters]
	2. (Network Monitor) [https://docs.microsoft.com/en-us/windows/client-management/troubleshoot-tcpip-netmon]

