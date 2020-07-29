<properties
	pageTitle="Solution for VPN Point-to-Site client error 13801"
	description="Solution for VPN Point-to-Site client error 13801"
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
	articleId="c6cc91b7-0d9b-4c01-b317-965a25464762"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 13801

The error *"Error 13801: IKE authentication credentials are unacceptable"* means that some required certificate is missing from the certificate store.

## Recommended Steps

1. Verify that the client certificate is in the **user’s** 'personal' certificate store by opening the certificate manager console (Start>Run>certmgr.msc>User>Personal>Certificates).
2. Else If the customer is using a ["Device Tunnel"](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-always-on-device-tunnel) verify that the client certificate is in the **local machine** 'personal' certificate store by opening the certificate manager console (Start>Run>certmgr.msc>Local Machine>Personal>Certificates).
3. Ensure it has been imported with the private key as shown in the recommended document below
4. Verify that the certificate has a Subject Name specified
5. Check if the Certificate has expired by opening the certificate and checking the 'Valid From' field
6. Check that the customer has not entered any incorrect character (for example trailing spaces) while pasting the root certificate data in the Portal

Create and deploy a new certificate as outlined below if the steps above do not solve as the certificate may be corrupted

## Recommended Documents

* https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site#clientexport
* https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-always-on-device-tunnel
