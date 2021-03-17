<properties
	  pageTitle="Fixed with fresh package"
	  description="Fixed with fresh package"
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
	  articleId="36142fb5-046d-4e67-8449-87a491635694"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Fixed with fresh package

The issue is fixed after the installation of a fresh User VPN Package.

The problem could have been related to recent changes applied to the considered Virtual HUB's P2S configuration, with client configuration not updated accordingly.

Make sure customer is aware that any reconfiguration of P2S parameters will need reinstall of relevant new VPN client packages on clients' side.

