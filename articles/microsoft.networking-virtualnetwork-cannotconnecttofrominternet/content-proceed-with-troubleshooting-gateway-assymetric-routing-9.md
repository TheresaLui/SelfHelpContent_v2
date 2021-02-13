<properties
	  pageTitle="Proceed with troubleshooting Assymetric Routing"
	  description="Proceed with troubleshootingAssymetric Routing"
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

Depending on the scenario, platform routes can be learned from components such as Vnet Peering, Express Route Gateway, VPN Gateway, that get plumbed into the NIC effective routes, including a 0.0.0.0/0 (forced tunneling).  We need to be aware how a particular destination is being learn from and be mindful of how Azure selects a route. Ie. A particular longer prefix can be learned from BGP propagation, conflicting the intended destination, and causing asymmetric routing. Document the next hop IP and identify what is the component 

## Recommended Steps

1. Navigate to the destination VM in ASC Resource Explorer
2. Select the ""Diagnostics"" Tab
3. Select the  ""Test Traffic""
4. Fill out the required boxes. (Highlight ""i"" icon for tips if you are unsure of any box)
5. Click ""Run"" for results
6. Review the next hop on STATELESS LAYER to determine what the IP of the Next Hop is and what is VFP LAYER is following

- ROUTE TARGET VPN
- ROUTE TARGET VNET
- ROUTE TARGET VNET PEERING
- ROUTE TARGET INTERNET


## Reccommended Documents

1. [ASC  TestTraffic ](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)

## Reccommended Documents

1. https://docs.microsoft.com/en-us/azure/virtual-network/diagnose-network-routing-problem
2. https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview#how-azure-selects-a-route
3. https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview#default-route

