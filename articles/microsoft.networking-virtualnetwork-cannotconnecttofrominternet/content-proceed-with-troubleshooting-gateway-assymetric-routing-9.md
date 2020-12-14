<properties
	  pageTitle="Proceed with troubleshooting Gateway Assymetric Routing"
	  description="Proceed with troubleshooting Gateway Assymetric Routing"
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
	  articleId="516c0444-4acd-4e0d-b1ba-2c16ed30194b"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Proceed with troubleshooting Gateway Assymetric Routing

Proceed with identifying assymetric routing. 

##Recommended Steps

1. Make sure there that customer has a route back to Azure on their destination network that matches the prefix they are trying to get to.

2. There should not be a more specific route learned by system routes or BGP learned.

3. If it is an all zero route follow this article 

https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview#default-route

