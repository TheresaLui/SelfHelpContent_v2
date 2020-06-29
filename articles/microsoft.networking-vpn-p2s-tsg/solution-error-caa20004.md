<properties
	pageTitle="Error CAA20004"
	description="Error CAA20004"
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
	articleId="a78466fe-625d-4f15-b211-4ec1801a9a7c"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error CAA20004

The error *"Error CAA20004: Invalid resource. The client has requested access to a resource which is not listed in the requested permissions in the client."* is an Azure AD specific error where the VPN client app doesn't have the necessary rights on Azure AD.

## Recommended Steps

1. Ask the Azure AD Administrator to provide Admin Consent for the AAD Tenant for Azure VPN AAD App.


## Recommended Documents

* [Grant tenant-wide admin consent to an application](https://docs.microsoft.com/azure/active-directory/manage-apps/grant-admin-consent)
