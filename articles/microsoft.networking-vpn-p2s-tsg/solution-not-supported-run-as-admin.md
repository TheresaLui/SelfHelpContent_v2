<properties
	pageTitle="Not Supported - Run as Admin"
	description="Not Supported - Run as Admin"
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
	articleId="6f879bd6-6686-4f53-bbef-43d65a962c5d"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Customer must have admin rights

We found that the logged-on user does not have local administrative rights on the VPN client machine. This is a requirement for the VPN client application. Point to Site won’t work without the logged-on user having Admin privileges.


## Recommended Steps

1. Give the local logged on user administrative rights on the client

## Recommended Documents

* [What are the client configuration requirements?](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#what-are-the-client-configuration-requirements)
