<properties
	  pageTitle="Determine next hop"
	  description="Determine next hop"
      service="Microsoft.network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="d838914d-2403-4f81-8309-6f9001791e9b"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Determine next hop

## Recommended Documents

https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview

User Defined Routes (UDRs) can be used to overwrite Azure system routs and force a custom next hop determined by the customer. 

The next hop determines what device will receive traffic for  the destination address space.


## Recommended Steps 

1. Review the 0.0.0.0 route to find the next hop.
2. Note the IP listed.
3. Return to the VNET of the VM and scroll down to the subnets to determine the location of the NIC.
4. If the IP is not found in the VNET check for VNET Peerings at the bottom of the VNET properties page. 

 
## Reccommended Documents

1. [Azure Custom Routes](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview#custom-routes)

