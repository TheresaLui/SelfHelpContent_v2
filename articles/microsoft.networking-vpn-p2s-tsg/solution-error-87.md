<properties
	pageTitle="Solution for VPN Point-to-Site client error 87"
	description="Solution for VPN Point-to-Site client error 87"
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
	articleId="d8726086-4327-4a81-9155-f452ad0ff426"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 87

The error *"Error 87: the parameter is incorrect"* is caused by a Guest OS issues on the client.

## Recommended Steps

1. Reinstall the VPN package
2. For MAC OS clients, there can be issues installing the root certificate. Engage your MAC OS team to install the root certificate and debug if needed
3. Validate that the AadTenantUri is correct according to [reference article](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-tenant)