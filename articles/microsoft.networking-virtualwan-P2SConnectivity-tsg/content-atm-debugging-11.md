<properties
	  pageTitle="ATM debugging"
	  description="ATM debugging"
      service="Microsoft.Network"
      resource="Microsoft.Network/VirtualWans"
	  authors="Danieleg"
	  ms.author="Danieleg"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="fd52fdcc-d0bc-4ccd-86bf-7d26dc7bd2ce"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# ATM debugging

Client is using a "Virtual WAN User VPN Profile" (GW's FQDN of type "wan.xxx.vpn.azure.com"),and after a fresh install of up-to-date package the client still connects to an incorrect HUB of the vWAN.

This could be related with:

1)Client's LDNS unexpectedly mapped to a region which is closer (in terms of performances) to the P2S-GW the client is seen to be connected to

2)A bug in the ATM profile bound to the "wan.xxx.vpn.azure.com" FQDN

This basically becomes an AzureTrafficManager support case.

To debug it, please use the guidelines provided in this Wiki:

https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/140174/TSG-Incorrect-Routing-with-Azure-Traffic-Manager?anchor=traffic-manager-routing-is-incorrect-%26-how-to-query-the-azure-traffic-manager-perf%2Fgeo-databases 

In case issue was not caused by an unexpected LDNS mapping, or if you suspected bugs with ATM, please engage TA accordingly for a review.


