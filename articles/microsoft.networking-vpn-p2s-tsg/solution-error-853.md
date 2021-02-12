<properties
	pageTitle="Solution for VPN Point-to-Site client error 853"
	description="Solution for VPN Point-to-Site client error 853"
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
	articleId="4021c66d-516a-435e-8982-3338fe664d4f"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 853

The error *"Error 853 the remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is not valid. Ensure that the certificate used for authentication is valid"* is due to invalid credentials being used. You may be using a domain-joined Point to Site client that has GPOs in place enforcing the usage of domain credentials rather than certificate credentials.

## Recommended Steps

1. Have your administrator check for GPOs enforcing domain credentials over certificate credentials

