<properties
	  pageTitle="Review packet captures to see if VM is receiving traffic."
	  description="Review packet captures to see if VM is receiving traffic."
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
	  articleId="76b87aee-7bd2-463e-a9ac-d9550d26b7bd"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Review packet captures to see if VM is receiving traffic.

Seeing the traffic from the source is a good sign that the path out to the destination is  

# Recommended Steps

1. Filter the packet capture for traffic between the IP addresses of the source and destination. See documentation for details on setting filters if needed. 
2. Search to see if you can see traffic that contains the source IP used for the test in the source column going to the tested destination IP address. 

# Reccommended Documents

1. (Wireshark Filters)[https://wiki.wireshark.org/DisplayFilters]
2. (Network Monitor) [https://docs.microsoft.com/en-us/windows/client-management/troubleshoot-tcpip-netmon]

