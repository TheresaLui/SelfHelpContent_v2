<properties
	  pageTitle="Solution for UDR on VNet range"
	  description="Solution for UDR on VNet range"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="5b3e1fc9-cc2d-4e2f-bac3-cec756ec60b6"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Solution for UDR on VNet range

Routes with destination range that falls within the VNet IP address range should not point to a VPN/ExpressRoute Gateway.

## Recommended Steps

1. Assist the customer with removing any routes that point the whole or parts of the VNet range to a VPN/ExpressRoute Gateway
2. Ask them to test connectivity

