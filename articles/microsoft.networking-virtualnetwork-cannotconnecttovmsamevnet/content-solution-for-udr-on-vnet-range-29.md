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
	  articleId="732d28aa-74cd-4a5e-8999-14dc547e78e2"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Solution for UDR on VNet range

Routes with destination range that falls within the VNet IP address range should not point to a VPN/ExpressRoute Gateway.

## Recommended Steps

1. Assist the customer with removing any routes that point the whole or parts of the VNet range to a VPN/ExpressRoute Gateway
2. Ask them to test connectivity

