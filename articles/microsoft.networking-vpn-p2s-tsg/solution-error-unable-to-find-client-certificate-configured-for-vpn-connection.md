<properties
	pageTitle="Unable to find Client Certificate configured for VPN Connection"
	description="Unable to find Client Certificate configured for VPN Connection"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="crcritel,stegag"
	ms.author="crcritel,stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="eed872e6-484f-417b-9e51-236099d181de"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error string "Unable to find Client Certificate configured for VPN Connection"

The error *"Unable to find Client Certificate configured for VPN Connection"* is an Azure AD specific error where the VPN client certificate is incorrect.

## Recommended Steps

1. Check if the client certificate is present in the user’s 'personal' certificate store by opening the certificate manager console (Start>Run>certmgr.msc>Personal>Certificates). 
2. Check if the certificate is not expired (open the certificate and check the 'Valid From' fields)

## Recommended Documents

* [Generate and export certificates for Point-to-Site using PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site)
