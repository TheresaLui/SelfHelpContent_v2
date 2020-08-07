<properties
	pageTitle="Error 3399614475"
	description="Error 3399614475"
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
	articleId="8d870306-db86-4898-bd04-86b586850978"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error 3399614475

The error *"Error 3399614475: Failure in Acquiring AAD Token. The resource principal named <> was not found in the tenant named <>. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You might have sent your authentication to the wrong tenant"* is an Azure AD specific error where the VPN client app doesn't have the necessary rights on Azure AD.

## Recommended Steps

1. Using the link below, configure Azure VPN AD authentication towards the correct AD tenant.


## Recommended Documents

* [Create an Azure Active Directory tenant for P2S OpenVPN protocol connections](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-tenant)
