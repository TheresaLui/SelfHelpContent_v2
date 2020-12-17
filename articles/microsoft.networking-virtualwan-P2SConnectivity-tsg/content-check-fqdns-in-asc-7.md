<properties
	  pageTitle="Check FQDNS in ASC"
	  description="Check FQDNS in ASC"
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
	  articleId="59395d78-3c8f-4152-898c-4d9e861a2f0c"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Check FQDNS in ASC

We tested with fresh client package and issue is persistent.

Let?s validate name resolution of the considered P2SGW.
Ask customer to share with you the file azurevpnconfig.xml from their recently downloaded User VPN client package.
Open the file, and lookup for tag ?FQDN?.
Take note of the relevant string: this will be something like ?wan.xxxxxxx.vpn.azure.com? (if customer used vWAN user profiles) or ?hubx.xxexxx.vpn.azure.com? (if they used HUB user profiles)
Open the ASC section of the P2SVPNGateway customer wants to connect to, and lookup for ?Virtual Wan Traffic Manager URL? or ?Virtual HUB Traffic Manager URL?, validate that the FQDN you retrieved from the XML file matches with the ones in ASC.

