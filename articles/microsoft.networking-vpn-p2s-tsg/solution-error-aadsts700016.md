<properties
	pageTitle="Error AADSTS700016"
	description="Error AADSTS700016"
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
	articleId="aa6aeaf5-a665-47b9-85bc-b80455edcd30"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error AADSTS700016

The error, "Error AADSTS700016: Application with identifier "xxxx" was not found in the directory "yyyy", is an Azure Active Directory-specific error where the `AadAudienceId` parameter is not configured correctly.

## Recommended Steps

* Connect to the Azure Portal
* Browse to the VPN gateway Point to Site configuration Blade
* Make sure that the **Audience** field is statically set to the value of `41b23e61-6c1e-4545-b367-cd054e0ed4b4`

## Recommended Documents

* [Create an Azure Active Directory tenant for P2S OpenVPN protocol connections](https://docs.microsoft.com/en-us/azure/vpn-gateway/openvpn-azure-ad-tenant)
