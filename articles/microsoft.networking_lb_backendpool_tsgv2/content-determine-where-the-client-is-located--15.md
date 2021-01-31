<properties
	  pageTitle="Determine where the client is located."
	  description="Determine where the client is located."
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="a611b775-7f0c-47c2-9d12-cf639305f280"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Determine where the client is located.

Use the customer verbatim and ASC to determine where the client VM is. If it is not clear from the verbatim, go to the backend VM resource diagnostics tab and view the effective routes. This lists all the address prefixes that are defined. 

If the NextHopeType is Local, the client is in the same VNet.

If the NextHopType is VNetPeering, browse to the VNet resource in ASC and note the location of the VM?s VNet in the properties section. Scroll down to the peering section and expand the relevant peering for the prefix covering the client IP. Ensure that "Allow Virtual Network Access" is set to true. Then select the link to browse to the remote VNet (you may have to add an additional subscription to Resource Explorer). Note the location of the peered VNet. If the location is the same as the backend VM, the client is in a regionally peered VNet. Otherwise, the client is in a globally peered VNet.

If the NextHopType is VPNGateway, the client is most likely on-premises. There is a very small chance the client could be on a VNet linked via a VPN gateway as this was an option prior to the VNet Peering feature was released.

