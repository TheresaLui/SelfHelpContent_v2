<properties
	pageTitle="Solution for VPN Point-to-Site client error 0x8008025b"
	description="Solution for VPN Point-to-Site client error 0x8008025b"
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
	articleId="782b56b3-03a4-4034-8dc3-048639e253b3"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x8008025b

The error *"Error 0x8008025b: Custom script (to update your routing table) failed"* is due to incorrect Active Directory domain settings applied to the client.

## Recommended Steps

1. Ensure you can connect to domain resources
2. Unjoin and re-join the Active Directory domain from the Point to Site client while connected to the Domain network.
3. Re-install the VPNclient package.
