<properties
	  pageTitle="Check if it's correct VIP resolved"
	  description="Check if it's correct VIP resolved"
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
	  articleId="608854c1-eb95-4372-9299-3d69980120f6"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Check if it's correct VIP resolved

Client is able to resolve the P2S GW's ATM FQDN.
We need to check that this IP matches effectively with the real VIP mapped to desired GW.

Open ASC at the section of the considered P2SVPNGateway
Scroll down to section *"P2S VPN Gateway Child gateways"*
Check the columns *"P2S VIP"*

Compare the VIP with what you have resolved on test client

If needed, compare with tests performed from your client laptop.

