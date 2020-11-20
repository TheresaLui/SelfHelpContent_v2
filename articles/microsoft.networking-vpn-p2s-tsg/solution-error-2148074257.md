<properties
	pageTitle="Error 2148074257"
	description="Error 2148074257"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="56689d16-81cb-4c83-93ef-56deabb426e9"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error 2148074257

The error, "Error 2148074257: No authority could be contacted for authentication", is an Azure AD specific error. It is caused by the client application failing to authenticate using the currently cached credentials.

## Recommended Steps

* Open the Azure VPN Client
* Click on the relevant point to site connection
* Click on the "**...**" icon and select **Configure**
* Click **Clear Saved Account** on the configuration page

## Recommended Documents

* [Configure OpenVPN clients for Azure VPN Gateway](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-openvpn-clients)
