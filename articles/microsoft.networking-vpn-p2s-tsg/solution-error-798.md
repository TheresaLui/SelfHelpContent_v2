<properties
	pageTitle="Solution for VPN Point-to-Site client error 798"
	description="Solution for VPN Point-to-Site client error 798"
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
	articleId="ef681877-1c4a-45ef-a5a7-24e061bcfa5b"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 798

The error *"Error 798: A certificate could not be found that can be used with this Extensible Authentication Protocol"* is the most common Azure Point to Site client error. It means that some required certificate is missing from the certificate store.

## Recommended Steps

1. Verify that the client certificate is in the user’s 'personal' certificate store by opening the certificate manager console (Start>Run>certmgr.msc>Personal>Certificates).
2. Ensure it has been imported with the private key as shown in the recommended document below
3. Verify that the certificate has a Subject Name specified
4. Check if the Certificate has expired by opening the certificate and checking the 'Valid From' field
5. Create and deploy a new certificate as outlined below if the steps above do not solve as the certificate may be corrupted

## Recommended Documents

* https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site#clientexport
