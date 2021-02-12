<properties
	pageTitle="OpenVPN does not support this scenario"
	description="OpenVPN does not support this scenario"
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
	articleId="a1f3ff58-d0fe-40f1-a277-7e6cefbd82f8"
  ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for OpenVPN does not support this scenario

We found that this is not a supported scenario. Native Azure AD authentication is only supported for the OpenVPN protocol and Windows 10 clients. It also requires the use of the Azure VPN Client exclusively. Third party Open VPN clients only support Certificates or RADIUS authentication.

## Recommended Steps

1. Configure the Azure VPN Client by using the XML file (not the *.ovpn file) as described in the [config article](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-client)


## Recommended Documents

* [About Point-to-site](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about)
* [The ovpn files will NOT be included in the package](https://docs.microsoft.com/azure/vpn-gateway/about-vpn-profile-download)
